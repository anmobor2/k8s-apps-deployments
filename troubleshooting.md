# to debug
helm template jenkins . -f ../values/values-dev.yaml --debug

### to install
helm install jenkins . -f ../values/values-dev.yaml

helm status jenkins
kubectl get pods -n default
kubectl logs jenkins-0 -n default -c <container-name> 
kubectl logs jenkins-0 -n default -c jenkins
kubectl describe pod jenkins-0 -n default
kubectl get pvc -n default

kubectl logs jenkins-0 -n default -c init
kubectl logs jenkins-0 -n default -c init --previous


### to upgrade
helm plugin install https://github.com/databus23/helm-diff
helm dependency update
helm upgrade jenkins . -f ../values/values-dev.yaml --debug

### to delete
helm uninstall jenkins


### connect to minikube
kubectl get svc -n default
kubectl get pods -n default
minikube tunnel
kubectl port-forward svc/jenkins 8080:8080 -n default
http://localhost:8080/login



### retrieve admin password
k8s-apps-deployments kubectl get secret jenkins -n default -o jsonpath="{.data.jenkins-admin-password}" | base64 --decode
BqVjA3QdtfeX485UoPKSoO

admin admin