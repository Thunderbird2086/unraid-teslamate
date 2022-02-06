# Unraid TeslaMate
[unRaid](https://unraid.net) Docker template for TeslaMate which is the amazing work done by [Adrian Kumpf](https://github.com/adriankumpf/teslamate).

## General features
 * High precision drive data recording
 * No additional vampire drain: the car will fall asleep as soon as possible
 * Automatic address lookup
 * Easy integration into Home Assistant (via MQTT)
 * Geo-fencing feature to create custom locations
 * Supports multiple vehicles per Tesla Account
 * Charge cost tracking
 * Import from TeslaFi and tesla-apiscraper

## How to install
* Requirements:
  1. PostgreSQL 10+
  1. Grafana
     - signed plugin: TrackMap by prOps 
     - unsigned plugin: [Panodata Map Panel](https://github.com/panodata/panodata-map-panel)
  1. Mosquitto

* Steps
  1. Install PostgreSQL
     - [Create PostgreSQL database](https://docs.teslamate.org/docs/installation/debian#create-postgresql-database): optional
     - Take a note of `POSTGRES_USER`, `POSTGRES_PASSWORD` and `POSTGRES_DB`
  1. Install Grafana continer
     - unsigneed plugin [Panodata Map Panel](https://github.com/panodata/panodata-map-panel) requires to add two container variables of `GF_INSTALL_PLUGINS` and `GF_PLUGINS_ALLOW_LOADING_UNSIGNED_PLUGINS`
      ![unraid container template](/img/two-additional-container-variables.png)
     - [Import Grafana Dashboards](https://docs.teslamate.org/docs/installation/debian#import-grafana-dashboards)
     - `GF_INSTALL_PLUGINS` should be `<plugin url>;<plugin directory>`, then `GF_PLUGINS_ALLOW_LOADING_UNSIGNED_PLUGINS` should `<plugin directory>`.
  1. Install Mosquitto
  1. Install TeslaMate
     - Use `POSTGRES_USER`, `POSTGRES_PASSWORD` and `POSTGRES_DB` for database connection.
