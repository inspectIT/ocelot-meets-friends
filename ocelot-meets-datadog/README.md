# Ocelot meets Datadog

This is the demo scenario described in the blog post https://www.novatec-gmbh.de/en/blog/ocelot-meets-bits/
In this Demo Ocelot enhances the data collection for Datadog:
![Setup](https://www.novatec-gmbh.de/wp-content/uploads/ocelot-datadog-landscape.png)

To run this Demo do the following:
- Make sure docker is installed on your system
- Get an Datadog API key
- Put the API key into the .env file
- Start the demo with the following command:
  ```
  docker-compose -f docker-compose-datadog.yml up -d
  ```