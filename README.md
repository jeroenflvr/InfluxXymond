 # InfluxXymond
Xymon sample perl worker that puts memory stats into an Influx db

Even though I still like the default xymon rrd graphs, some people don't.  Grafana is really good at displaying graphs and can read InfluxDB databases.  Xymon's native rrd databases are a time series db, just like InfluxDB.

Grafana has alerting capabilities but is nowhere nearly as powerful as Xymon when it comes to real monitoring.  Dashboard-wise, grafana wins hands-down.

Remember, this is just an example.  I'll be learning Google's Go language while giving a refresh of Xymon a go (no pun intented).


## Getting Started

Xymon has a xymond_channel http://xymon.sourceforge.net/xymon/help/manpages/man8/xymond_channel.8.html interface that hooks into one of xymond's channels (status, data, ..) and puts this out to a worker module. Doesn't sound very complicated and it really isn't.
You can write a very simple script that grabs stdin and prints it to stdout.
```
#!/usr/bin/perl
while (<>){
 print $_;
}
```
```
  ./xymond_channel --channel=status ./print_stdin.pl
```
Apart from some parsing and storing it in a database, that's it.
### Prerequisites

 - Xymon, of course
 - influxdb
 - perl
 - grafana

some perl modules


### Installing

First get your xymon installed:
 http://xymon.sourceforge.net/

Install the perl modules

```
sudo cpan install AnyEvent InfluxDB::LineProtocol EV AnyEvent::InfluxDB
```
Install influxdb and grafana by following this [guide](http://vmkdaily.ghost.io/influxdb-and-grafana-on-centos/) for centos/rhel 

## Authors

* **Jeroen Van Renterghem** - *Initial work* - 

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments



