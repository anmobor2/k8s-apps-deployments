kubectl config use-context environment_name
example: kubectl config use-context dev

cd tecnology_to_install/helm/
example: cd jenkins/helm/

helm dependency update

helm install technology_to_install . -f ../values/values-environment.yaml
example: helm install jenkins . -f ../values/values-dev.yaml



