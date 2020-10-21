# Digital Engineering Training Course

![Capco](https://github.com/capcodigital/.github/blob/master/assets/capco_logo.jpg)

## Purpose

This repo holds the introductory Digital Engineering training course.  The purpose of the course is to provide a good introduction to technologies that are commonly used by Capco Digital on client engagements.

The course is not meant as an extensive training in the specific technologies, a list or resources have been curated that will be useful for that purpose, as have Udemy channels been setup aligned to the Engineering development paths.  

## Contributing

If you would like to contribute to any Capco Digital OSS projects please read:

* [Code of Conduct](https://github.com/capcodigital/.github/blob/master/CODE_OF_CONDUCT.md)
* [Contributing Guidelines](https://github.com/capcodigital/.github/blob/master/CONTRIBUTING.md)

## Requirements

- Java 8 is required to build and run the application.

## Commands

### Starting MongoDB

To start up the required mongo database, run the following:

```shell
docker-compose -f stack.yml up -d if-db
```

### Clean, Build & Run the Application

To clean, build and run the application execute the following command:

```shell
./gradlew clean build bootRun
```

### Running Application in Docker

To build the application as a docker file, run the following:

```shell
gradle docker
```

### Running Required Dependencies using Docker

To run the required dependencies using docker containers, run:

```shell
docker-compose -f stack.yml up -d
```

### Running the Application

To run the application itself, run:

```shell
docker run -d -p 8090:8090 --name digitalengineeringcourse manucapco/digitalengineeringcourse:latest
```

You should be able to access the following page [here](http://localhost:8090/swagger-ui.html)
