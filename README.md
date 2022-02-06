# Unraid TeslaMate
[unRaid](https://unraid.net) Docker template for TeslaMate which is the amazing work done by [Adrian Kumpf](https://github.com/adriankumpf/teslamate).

## How to install
* Dependencies:
 1. PostgreSQL 10+
 1. Grafana
 1. MostQuitto

* Required steps before install TeslaMate:
 1. [Create PostgreSQL database](https://docs.teslamate.org/docs/installation/debian#create-postgresql-database)
 1. [Import Grafana Dashboards](https://docs.teslamate.org/docs/installation/debian#import-grafana-dashboards)

## General features
 * High precision drive data recording
 * No additional vampire drain: the car will fall asleep as soon as possible
 * Automatic address lookup
 * Easy integration into Home Assistant (via MQTT)
 * Geo-fencing feature to create custom locations
 * Supports multiple vehicles per Tesla Account
 * Charge cost tracking
 * Import from TeslaFi and tesla-apiscraper

