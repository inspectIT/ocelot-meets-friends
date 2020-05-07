# Ocelot meets Elastic APM

In this demo setup we instrument the Spring pet clinic application with inspectIT Ocelot agents and collect the monitoring data in Elasticsearch. In this configuration, Ocelot exports traces in Jaeger format and pushes them to Elastic's APM server via its Jaeger integration. Metrics are exposed in Prometheus/OpenMetrics format and collected by Elastic Metricbeat.

To run this Demo do the following:
- Make sure docker and docker-compose are installed on your system
- Start the demo with the following command:
  ```
  docker-compose up -d
  ```
- Wait until the whole stack is running, this might take a couple of minutes
- Check the results in Kibana, depending on your Docker setup you may need to adjust the host for the following links to work:
  - [APM and traces in Kibana](http://127.0.0.1:5601/app/apm#/services?rangeFrom=now-15m&rangeTo=now&refreshPaused=true&refreshInterval=0)
  - [Ocelot metrics in Kibana](http://127.0.0.1:5601/app/infra#/infrastructure/metrics-explorer?metricsExplorer=(chartOptions:(stack:!f,type:line,yAxisMode:fromZero),options:(aggregation:rate,groupBy:prometheus.labels.service,metrics:!((aggregation:rate,color:color0,field:prometheus.metrics.http_in_responsetime_sum))),timerange:(from:now-15m,interval:%3E%3D10s,to:now)))