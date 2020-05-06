# Ocelot meets Elastic APM

In this demo setup we instrument the Spring pet clinic application with inspectIT Ocelot agents and collect the monitoring data in Elasticsearch. In this configuration, Ocelot exports traces in Jaeger format and pushes them to Elastic's APM server via its Jaeger integration. Metrics are exposed in Prometheus/OpenMetrics format and collected by Elastic Metricbeat.

To run this Demo do the following:
- Make sure docker and docker-compose are installed on your system
- Start the demo with the following command:
  ```
  docker-compose up -d
  ```