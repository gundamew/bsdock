# bsdock

Try to dockerized my PHP development environment. It only contains Nginx, PHP-FPM, and MySQL containers.

Inspired by [Laradock](https://github.com/laradock/laradock).

## Requirement

* macOS High Sierra (10.13.2)
* Docker CE for Mac (17.12.0-ce-mac47)

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

### 4. Create containers
```shell
$ docker-compose build && docker-compose up -d
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
