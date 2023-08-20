helm package .

helm install mychart ./mychart-0.1.7.tgz

helm uninstall mychart

helm install mychart ./mychart-0.1.7.tgz --create-namespace --namespace mychart

helm uninstall mychart -n mychart

helm install mychart ./mychart-0.1.7.tgz --create-namespace --namespace mychart --values new-values.yaml

helm uninstall mychart -n mychart

helm upgrade --install mychart ./mychart-0.1.7.tgz --create-namespace --namespace mychart --values new-values.yaml --set service.type="NodePort"


Bonus

GH Pages & Helm repo

enable gh pages for repo

git clone 

helm repo index --url https://aldinkapetanovic.github.io/my-helm-chart .

change version

helm repo index --url https://aldinkapetanovic.github.io/my-helm-chart --merge index.yaml . 


git push


Add helm repo

helm repo add my-helm-chart https://aldinkapetanovic.github.io/my-helm-chart

helm install my-helm-chart my-helm-chart/mychart -n my-helm-chart --create-namespace



helm repo update

helm upgrade -n my-helm-chart my-helm-chart my-helm-chart/mychart

helm list -A