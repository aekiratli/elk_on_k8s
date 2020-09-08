# ELK Stack on K8s

charts: https://github.com/elastic/helm-charts

## Installing

Edit values.yaml depending on your needs, configure logstash or filebeat, disable ingress or PVC if needed.

	helm repo add elastic https://helm.elastic.co
	helm install myproject -f elasticsearch-values.yaml -n services elastic/elasticsearch
	helm install myproject -f kibana-values.yaml -n services elastic/kibana

Add 1 one of worker's IP or load balance IP with ingress name to your hosts file and test it. Don't forget to change elasticsearch's hostname from values.yamls if you have used different namespace
