helm package .

helm install mychart ./mychart-0.1.7.tgz

helm uninstall mychart

helm install mychart ./mychart-0.1.7.tgz --create-namespace --namespace mychart

helm uninstall mychart -n mychart

helm install mychart ./mychart-0.1.7.tgz --create-namespace --namespace mychart --values new-values.yaml

helm uninstall mychart -n mychart

helm upgrade --install mychart ./mychart-0.1.7.tgz --create-namespace --namespace mychart --values new-values.yaml --set service.type="NodePort"


Bonus

helm repo index --url https://aldinkapetanovic.github.io/my-helm-chart .

helm repo add my-helm-chart https://aldinkapetanovic.github.io/my-helm-chart

helm install my-helm-chart my-helm-chart/mychart -n my-helm-chart --create-namespace

