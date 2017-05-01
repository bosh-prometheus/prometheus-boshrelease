# Prometheus BOSH Release

This is a [BOSH](http://bosh.io/) release for [Prometheus](https://prometheus.io/).

It includes the following [Prometheus Exporters](https://prometheus.io/docs/instrumenting/exporters/):
* [Blackbox](https://github.com/prometheus/blackbox_exporter)
* [BOSH](https://github.com/cloudfoundry-community/bosh_exporter)
* [BOSH TSDB](https://github.com/cloudfoundry-community/bosh_tsdb_exporter)
* [cAdvisor](https://github.com/google/cadvisor)
* [Collectd](https://github.com/prometheus/collectd_exporter)
* [Consul](https://github.com/prometheus/consul_exporter)
* [Cloud Foundry](https://github.com/cloudfoundry-community/cf_exporter)
* [Cloud Foundry Firehose](https://github.com/cloudfoundry-community/firehose_exporter)
* [Elasticsearch](https://github.com/justwatchcom/elasticsearch_exporter)
* [Github](https://github.com/infinityworksltd/github-exporter)
* [Graphite](https://github.com/prometheus/graphite_exporter)
* [HAProxy](https://github.com/prometheus/haproxy_exporter)
* [Kubernetes](https://github.com/kubernetes/kube-state-metrics)
* [Memcached](https://github.com/prometheus/memcached_exporter)
* [MongoDB](https://github.com/dcu/mongodb_exporter)
* [MySQL](https://github.com/prometheus/mysqld_exporter)
* [NATS](https://github.com/lovoo/nats_exporter)
* [PostgreSQL](https://github.com/wrouesnel/postgres_exporter)
* [PushGateway](https://github.com/prometheus/pushgateway)
* [RabbitMQ](https://github.com/kbudde/rabbitmq_exporter)
* [Redis](https://github.com/oliver006/redis_exporter)
* [Statsd](https://github.com/prometheus/statsd_exporter)

## Usage

To use this BOSH release, first upload it to your BOSH:

```
bosh target <YOUR_BOSH_HOST>
bosh upload release https://bosh.io/d/github.com/cloudfoundry-community/prometheus-boshrelease
```

For [bosh-lite](https://github.com/cloudfoundry/bosh-lite), you can quickly create a deployment manifest & deploy a cluster:

```
git clone https://github.com/cloudfoundry-community/prometheus-boshrelease.git
cd prometheus-boshrelease
./templates/make_manifest warden
bosh -n deploy
```

For AWS EC2, create a deployment manifest & deploy a cluster:

```
git clone https://github.com/cloudfoundry-community/prometheus-boshrelease.git
cd prometheus-boshrelease
./templates/make_manifest aws-ec2
bosh -n deploy
```


### Known issues

The `cf_exporter` is known to require quite some resources on the `cloud_controller` since the queries include an `inline-relations-depth=2` API call, which basically dumps the `ccdb` and transforms it into `json` response. This may result in a very poor `cloud_controller` API performance. To prevent this, consider setting a reasonable `scrape_interval`.


## Contributing

Refer to [CONTRIBUTING.md](https://github.com/cloudfoundry-community/prometheus-boshrelease/blob/master/CONTRIBUTING.md).

## License

Apache License 2.0, see [LICENSE](https://github.com/cloudfoundry-community/prometheus-boshrelease/blob/master/LICENSE).
