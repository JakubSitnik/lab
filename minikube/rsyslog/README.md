1.`minikube start --driver=docker`
2.`eval $(minikube docker-env)`
3.`docker build -t rsyslog:1.0 .`
4.`kubectl apply -f deployment.yaml`.

Now if you go to the rsyslog container by: `kubectl exec -it [deployment_name] -- bash`, 
you can create any log in the serviceName.log file under /var/logs directory and rsyslog will
redirect them.
