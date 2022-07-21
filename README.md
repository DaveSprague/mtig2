# MIG (Mosquitto, InfluxDB, Grafana)

MIG is a containerised IoT sensor server stack in the traditions of LAMP and TIG.

This is a Docker Compose collection of containers that implement:

- Mosquitto MQtt broker listening on port 1883 for MQtt message publications

- InfluxDB listening on port 8086 providing a time series database for sensor data storage

- A Mosquitto bridge that listens for MQTT messages and sends contained data to influxDB

- Grafana listening on port 3000 providing a data visualisation environment for sensor data.

Each of these applications is built and runs in its own container.


# Getting going

Install Docker and Docker Compose

Clone this repository

run "docker compose up" in the repository directory

Open your browser to "localhost:3000" to bring up Grafana
username and password are both currently "admin"

Run the test publisher client, mqtt-test-publish-client.py, on the same computer
(or change its broker url if running on a separate device) and then create
a dashboard in grafana, on port 3000, to see the data.

It's that easy!

# More detail

VS Code has a docker extension that makes it easy:
 - to bring up the docker composed containers
 - open up a shell in a container
 - stop/start/restart individual containers
 - bring up or down the entire composition of containers

# Next Steps
 - update to latest versions of mosquitto, influxdb1.8, etc
 - Trying bring in up on a RPi
 - Integrate ngnix for reverse proxy
 - Support both a public view-only dashboard and a private, password-protected, access for creating dashboards.
 - cleanup project
   - remove Dockerfile.raspberrypi3 and Dockerfile.template files since I don't think they're needed.
 - try out the jupyterlab container, this was part of the original project and sounds handy.

# Maintainer / Contributors

- David Sprague @DaveSprague

# Attribution

- Started as a fork of this project: https://github.com/DynamicDevices/ming


# Contributing




