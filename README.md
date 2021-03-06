# Athena [![Build Status](https://drone.io/github.com/StarTrackDevKL/athena/status.png)](https://drone.io/github.com/StarTrackDevKL/athena/latest) [![Dependency Status](https://gemnasium.com/StarTrackDevKL/athena.svg)](https://gemnasium.com/StarTrackDevKL/athena) <img src="publicdomain.png" height="20px" />
A simple library system powered by [JHipster][1].

## Requirements
- [Java 8](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
- [Apache Maven 3](https://maven.apache.org/download.cgi)
- [PostgreSQL](http://www.postgresql.org/download/)
- [JHipster][1]

## Setup
Some folders are excluded from the repository. Folders such as **node_modules** and **bower_components**. Reason being is these folders can get too big in future.
Build Athena with `prod` profile in order to generate them. Also **you have to be root or administrator** in order to execute the following command:

```sh
mvn clean package -Pprod
```

Execute `bower install` in order to add new front-end dependency.

## Contributing
Please submit a Pull Request against [develop](https://github.com/StarTrackDevKL/athena/tree/develop) branch.

## Building the project
Athena uses [Apache Maven](https://maven.apache.org/) and she accepts the following parameters; `db.host`, `db.port`, `db.name`, `db.username`, and `db.password`. Each parameters are self explanatory.
Example of maven command to build her:

```sh
mvn clean package -Ddb.host=localhost -Ddb.port=5432 -Ddb.name=athena -Ddb.username=athena -Ddb.password=2948f5a3b9b3ca2d991c40c8d523bf07
```

To build production, you will have to include `-Pprod`. This will execute the `production` profile. By default it will be using `dev` profile.

[1]: http://jhipster.github.io/
