# Install Prometheus using Helm

## Add helm repo

`helm repo add prometheus-community https://prometheus-community.github.io/helm-charts`

## Update helm repo

`helm repo update`

## Install helm 

`helm install prometheus prometheus-community/prometheus`

## Expose Prometheus Service

This is required to access prometheus-server using your browser.

`kubectl expose service prometheus-server --type=NodePort --target-port=9090 --name=prometheus-server-ext`

# Install Grafana using Helm

## Add helm repo

`helm repo add grafana https://grafana.github.io/helm-charts`

## Update helm repo

`helm repo update`

## Install helm 

`helm install grafana grafana/grafana`

## Expose Grafana Service

`kubectl expose service grafana — type=NodePort — target-port=3000 — name=grafana-ext`
