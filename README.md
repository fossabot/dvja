# Damn Vulnerable Java Application
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2FPriyanka20222%2Fdvja.svg?type=shield)](https://app.fossa.com/projects/git%2Bgithub.com%2FPriyanka20222%2Fdvja?ref=badge_shield)


## Quick Start

Install Docker and Docker Compose.

```
docker-compose up
```
Navigate to `http://localhost:8080`

To update image

```
docker-compose build
```

## Requirements

* Java 1.7+
* Maven 3.x
* MySQL Server

## Configuration

### Database

Create MySQL database and credentials and configure the same in:

```
./src/main/webapp/WEB-INF/config.properties
```

### Schema Import

Import the schema into MySQL database:

```
$ mysql -u USER -pPASSWORD dvja < ./db/schema.sql
```

## Build

```
$ mvn clean package
```

The deployable `war` file is generated in targets directory.

## Run with Jetty

```
$ mvn jetty:run
```

This will start the `Jetty` server on port 8080.

## Deploy in Tomcat Server

* Build app
* Copy targets/dvja.war to Tomcat webapps directory
* To serve as root application, copy as `ROOT.war` to Tomcat webapps directory.



## License
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2FPriyanka20222%2Fdvja.svg?type=large)](https://app.fossa.com/projects/git%2Bgithub.com%2FPriyanka20222%2Fdvja?ref=badge_large)