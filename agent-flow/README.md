kubectl -n monitoring apply -f grafana-agent-conf.yaml
kubectl -n monitoring apply -f grafana-agent-traces.yaml
helm -n monitoring install grafana-agent grafana/grafana-agent -f values.yaml
