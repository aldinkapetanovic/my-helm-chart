helm package .

helm install mychart ./mychart-0.1.7.tgz

helm uninstall mychart

helm install mychart ./mychart-0.1.7.tgz --create-namespace --namespace mychart

helm uninstall mychart -n mychart

helm install mychart ./mychart-0.1.7.tgz --create-namespace --namespace mychart --values new-values.yaml

helm upgrade --install mychart ./mychart-0.1.7.tgz --namespace mychart --values new-values.yaml --set persistence.accessMode="ReadOnlyMany" --set service.type="NodePort"