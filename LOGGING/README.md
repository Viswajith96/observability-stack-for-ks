# This is the helm chart for deploying Loki and promtail (PLG stack) to collect and process the application logs.

- The promtail-agent will run as a kubernetes daemon-set and will collect logs from each nodes and Loki will parse these logs and will act as a datasource for grafana.

- Loki is using a S3 bucket for storing the logs.

- here we are deploying the micro-service model of Loki for a more stable deployment and autoscaling.
 

Command to install the Loki helm chart.

`helm upgrade --install loki-distributed loki-distributed/loki-distributed -n monitoring -f loki-distributed/loki-distributed-custom-values.yaml`.

Command to install the Loki helm chart.

`helm upgrade --install promtail promtail-agent/promtail -n monitoring -f promtail-agent/promtail-custom-values.yaml` 

Note: make sure you have helm installed and created the namespace monitoring
