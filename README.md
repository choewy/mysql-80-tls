# README

## Docker Compose up

IN `workspace`

```
$ docker-compose up --build -d
$ docker ps
$ docker exec -it { CONTAINER_ID } /bin/bash
```

## Create CA Files

IN `container`

```
$ mysql_ssl_rsa_setup [ --uid=MYSQL_USER ]
$ exit
```

## Copy CA Files

IN `workspace`

```
$ mkdir certificate
$ cp ./data/*.pem ./certificate
```

## Re-run Docker Compose

IN `workspace`

```
$ docker compose up --build -d
```

## Reference

- [6.3.1 Configuring MySQL to Use Encrypted Connections](https://dev.mysql.com/doc/refman/5.7/en/using-encrypted-connections.html)
- [6.3.3.1 Creating SSL and RSA Certificates and Keys using MySQL](https://dev.mysql.com/doc/refman/5.7/en/creating-ssl-rsa-files-using-mysql.html)
- [6.3.3.2 Creating SSL Certificates and Keys Using openssl](https://dev.mysql.com/doc/refman/5.7/en/creating-ssl-files-using-openssl.html)
