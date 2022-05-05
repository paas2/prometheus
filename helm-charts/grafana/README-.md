# Generate datasource-secret.yaml

kubectl create secret generic datasource-secret --from-file=_datasource-secret.yaml --dry-run=client -oyaml > datasource-secret.yaml

# Generate Dashboards

kubectl create configmap node-exporter-full --from-file=../dashboards/node-exporter-full.json --dry-run=client -oyaml > dashboard-node-exporter-full.yaml