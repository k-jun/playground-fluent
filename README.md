## setup

```sh
$ docker-compose up -d
```

## fluentd -> fluentbit

```sh
$ docker-compose exec fluentbit /fluent-bit/bin/fluent-bit -c fluentbit_d2bit.conf
$ docker-compose exec fluentd fluentd -c /src/fluentd_d2bit.conf
```

## fluentbit -> fluentd

```sh
$ docker-compose exec fluentd fluentd -c /src/fluentd_bit2d.conf
$ docker-compose exec fluentbit /fluent-bit/bin/fluent-bit -c fluentbit_bit2d.conf
```
