# ttn2grafana

MQTT (TTN) &#8594; Telegraf &#8594; InfluxDb &#8594; Grafana

[tutorial](https://www.influxdata.com/blog/connecting-the-things-network-to-influxdb/)

## Getting Started

Copy the local telegraf config:

```
cp telegraf-local.config telegraf.config
```

then fill in with your own TTN credentials, [see here for more details](https://www.thethingsnetwork.org/docs/applications/mqtt/quick-start.html).

Start up services

```
docker-compose up
```

To publish mock TTN MQTT messages locally, first install [mosquitto](https://mosquitto.org/download/)

Use this command to publish the example message provided:
```
mosquitto_pub -t 'exampleAppId/devices/exampleDevId/up' -m "$(cat example-ttn-mqtt-message.json)"
```
