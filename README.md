# kafka-stress-test-helm
---
## Create Secret
kubectl create secret generic kafka-credentials \
  --from-literal=username='kafka-user' \
  --from-literal=password=''

## Start producer
helm upgrade --install nikhil-kafka-producer ./kafka-producer

## Start Consumer
helm upgrade --install nikhil-kafka-consumer ./kafka-consumer
