# RDP Tutorial

## About

This repository provides the source code for a step-by-step tutorial for the [Rapid Deployment Platform](https://ait-rdp.github.io/).

+ **Step 1**:
  Setup of the [Redis](https://redis.io/) stream and [Redis Insight](https://redis.io/insight/) for debugging.
  The code is available [here](https://github.com/AIT-RDP/rdp-tutorial/tree/step-1).
+ **Step 2**:
  Add an [RDP Data Crawler](https://ait-rdp.github.io/rdp-data-crawler) for retrieving weather data.
  The code is available [here](https://github.com/AIT-RDP/rdp-tutorial/tree/step-2).
+ **Step 3**:
  Add an [RDP Database](https://ait-rdp.github.io/rdp-database) and an [RedSQL Data Sync](https://ait-rdp.github.io/rdp-redsql) for long-time storage of the weather data.
  The code is available [here](https://github.com/AIT-RDP/rdp-tutorial/tree/step-3).
+ **Step 4**:
  Add a [Grafana](https://grafana.com/oss/grafana/) dashboard for visualizing the weather data.
  The code is available [here](https://github.com/AIT-RDP/rdp-tutorial/tree/step-4).
+ **Step 5**:
  Integrate a new micro-service for forecasting the power output of a PV module based on the weather data.
  The code is available [here](https://github.com/AIT-RDP/rdp-tutorial/tree/step-5).
+ **Step 6**:
  Integrate a custom data crawler for retrieving the power grid frequency from the public [Energy-Charts API](https://api.energy-charts.info/).
  The code is available [here](https://github.com/AIT-RDP/rdp-tutorial/tree/step-6).
+ **Step 7**:
  Configure a reverse proxy for securing access to the dashboard via TLS (using a self-signed certificate).
  The code is available [here](https://github.com/AIT-RDP/rdp-tutorial/tree/step-7).

## Prerequisites

You need to have [Docker](https://docs.docker.com/) and [Docker Compose](https://docs.docker.com/compose/) installed.

## Usage

Deploy the setup:
``` shell
docker compose up
```

Inspect the Redis streams in your browser via: http://localhost:5540/

In case you expose port 5432 of the RDP database (`timescale` serivce in [docker-compose.yml](./docker-compose.yml)), you can access it via tools like [DBeaver](https://dbeaver.io/) or [pgAdmin](https://www.pgadmin.org/).
