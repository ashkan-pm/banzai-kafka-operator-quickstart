## Kafka and Zookeeper operator installation via helm charts

### Kafka
```bash
kubectl create --validate=false -f https://github.com/banzaicloud/kafka-operator/releases/download/v0.15.1/kafka-operator.crds.yaml
```
```bash
helm install core --namespace=kafka banzaicloud-stable/kafka-operator
```

### Zookeeper
```bash
helm install zookeeper-operator --namespace=zookeeper pravega/zookeeper-operator
```

### Node selection
You can use `nodeSelector` or `affinity` to further control the deployment of your cluster on the Kubernetes nodes by searching for `YOUR_GKE_NODE_POOL` in the repository. The rest should be self-explanatory.
