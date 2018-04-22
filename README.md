# bsdock

Try to dockerized my PHP development environment. It only contains Nginx, PHP-FPM, and MySQL containers.

Inspired by [Laradock](https://github.com/laradock/laradock).

## Requirement

I run the containers on **macOS High Sierra (10.13.2)** and **Docker CE for Mac (17.12.0-ce-mac47)**.

The scripts may work on Ubuntu or any other OS, but I did not test on them.

## Usage

### 1. Create workspace
```shell
$ mkdir workspace
```

### 2. Clone the repository
```shell
$ cd workspace/
$ git clone git@github.com:gundamew/bsdock.git
```

### 3. Create & run containers
```shell
$ docker-compose up -d --build
```

## File Structure
```shell
.
├── bsdock
│   ├── docker-compose.yml
│   ├── mysql
│   ├── nginx
│   └── php-fpm
├── data
│   └── mysql
├── logs
│   └── nginx
└── www
    └── example
        └── index.php
```

* `data/`: Database system files
* `www/`: The web server document root
