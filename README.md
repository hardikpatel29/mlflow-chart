helm pull bitnami/mlflow --untar


For Host


packaging

helm package ./infra/helm/mlflow


generate index.yaml

helm repo index charts/ --url https://github.com/hardikpatel29/mlflow-chart/charts


move files 

mkdir -p docs
cp charts/* docs/


push in git

than

Enable GitHub Pages
Go to your GitHub repository.-> Navigate to Settings → Pages.-> Under Source, choose: -> Branch: main-> Folder: /docs

Click Save.


How to Use

follow


helm repo add my-mlflow https://hardikpatel29.github.io/mlflow-chart/ 
helm repo update
helm search repo my-mlflow
