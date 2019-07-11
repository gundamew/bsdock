# bsdock

Try to dockerized my PHP development environment. It only contains Nginx, PHP-FPM, and MySQL containers.

Inspired by [Laradock](https://github.com/laradock/laradock).

## Requirement

I run the containers on **macOS High Sierra (10.13.4)** and **Docker CE for Mac (18.03.1-ce-mac65)**.

The scripts may work on Ubuntu or any other OS, but I did not test on them.

It uses [mkcert](https://github.com/FiloSottile/mkcert) to create self-signed SSL certificates.

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

### 3. Create self-signed SSL certificates
```shell
# Create a new local CA first
$ mkcert -install

# Create new certificates for local development URLs
$ mkcert example.test localhost 127.0.0.1 ::1

# Create a strong Diffie-Hellman group
$ sudo openssl dhparam -out /path/to/dhparam.pem 4096
```

### 4. Create & run containers
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

* `data/` Database system files
* `www/` The web server document root
