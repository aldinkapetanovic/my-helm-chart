helm package .

helm install my-helm-chart ./my-helm-chart-0.1.9.tgz

helm uninstall my-helm-chart

helm install my-helm-chart ./my-helm-chart-0.1.9.tgz --create-namespace --namespace my-helm-chart

helm uninstall my-helm-chart -n my-helm-chart

helm install my-helm-chart ./my-helm-chart-0.1.9.tgz --create-namespace --namespace my-helm-chart --values new-values.yaml

helm uninstall my-helm-chart -n my-helm-chart

helm upgrade --install my-helm-chart ./my-helm-chart-0.1.9.tgz --create-namespace --namespace my-helm-chart --values new-values.yaml --set service.type="NodePort"


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

helm install my-helm-chart my-helm-chart/my-helm-chart -n my-helm-chart --create-namespace



helm repo update

helm upgrade -n my-helm-chart my-helm-chart my-helm-chart/my-helm-chart

helm list -A