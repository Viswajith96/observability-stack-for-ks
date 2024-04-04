# This is the helm charts for deploying prometheus and thanos helm chart for collecting and processing metrics.

- The prometheus comunity helm chart is customised with an eBPF based node agent to pull application error into prometheus readable format.

- Alert manager will send alerts to slack channels based on kubernetes events and application errors.

- Thanos will do similar kind of job as federated prometheus, collecting metrics from different clusters. it will be the datasource for grafana to visualise the metrics.
 

Command to install the prometheus helm chart.

`helm upgrade --install prometheus prometheus-ebpf -n monitoring`.

Command to install the thanos helm chart.

`helm upgrade --install thanos thanos/thanos -n monitoring -f thanos/thanos-custom-values.yaml` 

Note: make sure you have helm installed and created the namespace monitoring
