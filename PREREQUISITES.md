# Prerequisites

This is the prerequisites document for data engineer technical exercise.

To work on the exercise, you will need Git, Docker, SQL client for PostgreSQL and development environment for at least one of Ruby, Python, Java.

## Docker

Please follow the steps below.

1. Install `docker` command (if you don't have one)
2. Pull docker images
3. Check docker images

### Install command

Please install one for your OS from [https://docs.docker.com/get-docker/](https://docs.docker.com/get-docker/).

### Pull docker images

It is important to pull images before the start of exercise as this will download about 250MB of data.

```
docker pull public.ecr.aws/m4h2e8g9/data-engineering-technical-exercise-nginx:latest
docker pull public.ecr.aws/m4h2e8g9/data-engineering-technical-exercise-postgre:latest
```

### Check docker images

Check nginx environment.

```
$ docker run -p 8080:80 public.ecr.aws/m4h2e8g9/data-engineering-technical-exercise-nginx:latest
(open another terminal)
$ curl http://localhost:8080/index.txt
data_001.csv.gz
data_002.csv.gz
....
data_100.csv.gz
```

Check PostgreSQL environment.

```
$ docker run -p 5439:5432 public.ecr.aws/m4h2e8g9/data-engineering-technical-exercise-postgre:latest
(open another terminal)
$ psql -h localhost -p 5439 -U cookpad cookpad
Password for user cookpad:
Pager usage is off.
psql (13.2, server 13.3 (Debian 13.3-1.pgdg100+1))
Type "help" for help.

cookpad 14:44:08 #
```

Note: If you don't have the `psql` command, please check connection with your SQL client.

Here is connection information:

- host: `localhost`
- port: 5439
- database: `cookpad`
- username: `cookpad`
- password: `password`

## SQL Client for PostgreSQL

Please setup your favorite one from internet.

## Development environment

Please use any of Ruby, Python, Java and Bash to work on the exercise.

### Ruby

Please install Ruby 2.7 or higher. You can use rbenv if preferable.

Then please check the version after installation.
```
$ ruby --version
ruby 2.7.2p137 (2020-10-01 revision 5445e04352) [x86_64-darwin19]
```

### Python

Please install Python 3.8 or higher. You can use pyenv if preferable.

Then please check the version after installation.
```
$ python3 --version
Python 3.9.1
```

### Java

Please install JDK 11 or higher. You can use any of Oracle JDK, Open JDK, Amazon Corretto.

Then please check the version after installation.

```
$ java --version
openjdk 11.0.6 2020-01-14
OpenJDK Runtime Environment AdoptOpenJDK (build 11.0.6+10)
OpenJDK 64-Bit Server VM AdoptOpenJDK (build 11.0.6+10, mixed mode
$ javac -version
javac 11.0.6
```