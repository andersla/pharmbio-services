This repo contains docker services (launched via docker-compose) for monitoring infrastructure

Uncomment exporters not needed for speciffic server in the file `dockprom/docker-compose.yml` (e.g. gpu-exporter on messi, klose) and in `dockprom/prometheus/prometheus.yml`

Run in `dockprom/` with command `ADMIN_USER='admin' ADMIN_PASSWORD='xxxxxxxxxxxxxxxxxx' GRAFANA_TRAEFIK_FRONTEND_RULE='Host:monitor-klose.pharmb.io' docker-compose up -d`

Run in `traefik/` with command `docker-compose up -d` NOTE that you might need to create subdir `traefik/acme` and set correct permissions on it as described on Internet...
