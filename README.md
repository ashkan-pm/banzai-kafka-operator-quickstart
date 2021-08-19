## Kafka and Zookeeper operator installation via helm charts

### Kafka
`kubectl create --validate=false -f https://github.com/banzaicloud/kafka-operator/releases/download/v0.15.1/kafka-operator.crds.yaml`
`helm install core --namespace=kafka banzaicloud-stable/kafka-operator --values 5-kafka.values.yaml`

### Zookeeper
`helm install zookeeper-operator --namespace=zookeeper pravega/zookeeper-operator --values 2-zookeeper.values.yaml`
