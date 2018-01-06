 # InfluxXymond
Xymon sample perl worker that puts memory stats into an Influx db

Even though I still like the default xymon rrd graphs, some people don't.  Grafana is really good at displaying graphs and can read InfluxDB databases.  Xymon's native rrd databases are a time series db, just like InfluxDB.

Grafana has alerting capabilities but is nowhere nearly as powerful as Xymon when it comes to real monitoring.  Dashboard-wise, grafana wins hands-down.

Remember, this is just an example.  I'll be learning Google's Go language while giving a refresh of Xymon a go (no pun intented).


## Getting Started

Xymon has a xymond_channel http://xymon.sourceforge.net/xymon/help/manpages/man8/xymond_channel.8.html interface that hooks into one of xymond's channels (status, data, ..) and puts this out to a worker module. Doesn't sound very complicated and it really isn't.
You can write a very simple script that grabs stdin and prints it to stdout:

#!/usr/bin/perl
while (<>){
 print $_;
}

call it maybe print_stdin.pl and use it like so:
  ./xymond_channel --channel=status ./print_stdin.pl

Apart from some parsing and storing it in a database, that's it.

## The things you need:
 - Xymon, of course
 - influxdb
 - perl

### Prerequisites

 - Xymon, of course
 - influxdb
 - perl


```
Give examples
```

### Installing

A step by step series of examples that tell you have to get a development env running

Say what the step will be

```
Give the example
```

And repeat

```
until finished
```

End with an example of getting some data out of the system or using it for a little demo

## Running the tests

Explain how to run the automated tests for this system

### Break down into end to end tests

Explain what these tests test and why

```
Give an example
```

### And coding style tests

Explain what these tests test and why

```
Give an example
```

## Deployment

Add additional notes about how to deploy this on a live system

## Built With

* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
* [Maven](https://maven.apache.org/) - Dependency Management
* [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **Billie Thompson** - *Initial work* - [PurpleBooth](https://github.com/PurpleBooth)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Hat tip to anyone who's code was used
* Inspiration
* etc



