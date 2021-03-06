# Prerequisites

These are the prerequisites document for Cookpad's Data Engineering technical exercise.

To work on the exercise, you will need:

- Git
- Docker
- A development environment with either Ruby, Python, Java, or Bash available.

## Docker

For the exercise, we will use a docker container environment.
Please follow the sections below to make sure you have access to the images and you are able to run them.

## Install Docker

Please install one for your OS from [https://docs.docker.com/get-docker/](https://docs.docker.com/get-docker/).

### Run the docker image

Please run following command to download and run the docker image.

```
$ docker run -p 5439:5432 public.ecr.aws/z2e1v6f7/data-engineering-technical-exercise-postgre:1
```

### Check the docker image

The container has a PostgreSQL DB running on it
Please check connectivity for the DB.

Here is connection information:

- host: `localhost`
- port: 5439
- database: `cookpad`
- username: `cookpad`
- password: `password`

Tables can be found in the `cookpad` schema.

```
cookpad 14:57:04 # \dt
               List of relations
 Schema  |        Name        | Type  |  Owner
---------+--------------------+-------+---------
 cookpad | comments           | table | cookpad
 cookpad | cooksnaps          | table | cookpad
 cookpad | images             | table | cookpad
 cookpad | pv_log_001         | table | cookpad
 cookpad | pv_log_002         | table | cookpad
 cookpad | pv_log_003         | table | cookpad
 cookpad | pv_log_004         | table | cookpad
 cookpad | recipe_ingredients | table | cookpad
 cookpad | recipe_steps       | table | cookpad
 cookpad | recipes            | table | cookpad
 cookpad | users              | table | cookpad
(11 rows)
```

## Development environment

Make sure you have access to either Ruby, Python, Java, or Bash to work on the exercise.

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
