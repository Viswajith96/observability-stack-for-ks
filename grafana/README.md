# This is the helm chart for deploying grafana to monitor the application/infrastructure metrics and application logs.

The authentication to grafana is handled through google authentication and the application is exposed through an nginx ingress with letsencrypt for secure communication.

Command to install the helm chart.

`helm install grafana grafana -n monitoring -f grafana-custom-values.yaml`.

Note: make sure you have helm installed and created the namespace monitoring
