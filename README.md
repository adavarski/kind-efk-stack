# efk-kind-allinone

Install EFK (ElasticSearch Fluentd Kibana) Stack for Kind Cluster
## Create a new Kind Cluster

```bash
kind create cluster --config kind.yaml
```

## Install EFK Stack

```bash
kubectl apply -f allinone.yaml
```

## Kibana Dashboard

```bash
kubectl port-forward svc/kibana-logging -n kube-system 5601
```

Open a browser to access http://localhost:5601/

<img src="kind-efk-kibana?raw=true" width="1000">

