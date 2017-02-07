# Prometheus BOSH Release

This is a [BOSH](http://bosh.io/) release for [Prometheus](https://prometheus.io/).

It includes the following [Prometheus Exporters](https://prometheus.io/docs/instrumenting/exporters/):
* [Blackbox](https://github.com/prometheus/blackbox_exporter)
* [BOSH](https://github.com/cloudfoundry-community/bosh_exporter)
* [cAdvisor](https://github.com/google/cadvisor)
* [Collectd](https://github.com/prometheus/collectd_exporter)
* [Consul](https://github.com/prometheus/consul_exporter)
* [Cloud Foundry](https://github.com/cloudfoundry-community/cf_exporter)
* [Cloud Foundry Firehose](https://github.com/cloudfoundry-community/firehose_exporter)
* [Github](https://github.com/infinityworksltd/github-exporter)
* [Graphite](https://github.com/prometheus/graphite_exporter)
* [HAProxy](https://github.com/prometheus/haproxy_exporter)
* [Kubernetes](https://github.com/kubernetes/kube-state-metrics)
* [MongoDB](https://github.com/dcu/mongodb_exporter)
* [MySQL](https://github.com/prometheus/mysqld_exporter)
* [NATS](https://github.com/lovoo/nats_exporter)
* [PostgreSQL](https://github.com/wrouesnel/postgres_exporter)
* [PushGateway](https://github.com/prometheus/pushgateway)
* [RabbitMQ](https://github.com/kbudde/rabbitmq_exporter)
* [Redis](https://github.com/oliver006/redis_exporter)
* [Statsd](https://github.com/prometheus/statsd_exporter)

## Usage

```
$ bosh -d prometheus deploy manifests/example.yml
```

## Contributing

Refer to [CONTRIBUTING.md](https://github.com/cloudfoundry-community/prometheus-boshrelease/blob/master/CONTRIBUTING.md).

## License

Apache License 2.0, see [LICENSE](https://github.com/cloudfoundry-community/prometheus-boshrelease/blob/master/LICENSE).
