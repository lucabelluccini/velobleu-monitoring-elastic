# Velobleu Nice stands monitoring

This is a proof of concept on how to monitor the Velobleu Nice stands using the Elastic stack

Do not use in production, includes X-Pack trial license for 1 month

Uses default passwords!

Monitoring is enabled Kibana and Logstash thanks to X-Pack

## How to run

```
sudo sysctl -w vm.max_map_count=262144
docker-compose up
```

## Logged data

Fields logged:

* tc = total capacity
* ac = available capacity
* ap = available parking
* ab = available bike

## TODO

* Compute some values e.g. tc - (ap+ab)
* Index templates
* GeoPoints to be correctly taken into account through index template
* Dashboards
