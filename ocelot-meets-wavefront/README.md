# Ocelot meets Wavefront

This is the demo scenario described in the blog post https://www.novatec-gmbh.de/en/blog/ocelot-meets-wavefront/
In this Demo Ocelot enhances the data collection for Wavefront:
![Setup](https://www.novatec-gmbh.de/wp-content/uploads/openapm_wavefront.png)

To run this Demo do the following:
- Make sure docker is installed on your system
- Get an Wavefront API key
- Put the API key into the .env file
- Maybe you also have to adapt the Wavefront URL in the .env file
- Start the demo with the following command:
  ```
  docker-compose -f docker-compose-wavefront.yml up -d
  ```
