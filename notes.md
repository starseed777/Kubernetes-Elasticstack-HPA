fluentd >> collects the logs 
fluentd is an open source data collecter 

ElasticSearch >> database where everything gets stored 

kibana >> visualization tool 

Together these 3 = ELASTICSTACK

create a service acc + rbac for fluentd with necessary permissions + bind clusterrole to service acc

creating the pod for fluentd >> kind daemonset -- Each worker node will have unique daemonset to collect logs for all pods 

deployments would limit to only one pod when we would need multiple pods so we dont miss any log collections >> daemonset over deployment 

volume annotations for storage class >> if no volume annotations - manually patch the storage class 

for reference >> https://github.com/kubernetes/kubernetes/tree/master/cluster/addons/fluentd-elasticsearch






