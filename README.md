# clo835assignment3
kubectl create ns lab3
kubectl create -f standard_pvc.yaml -n lab3

kubectl create -f pvc.yaml
kubectl get pvc,pv -n lab3

kubectl delete service/webapp -n myapp
kubectl delete deployment.apps/webapp  -n myapp 
kubectl delete deployment.apps/mysql  -n lab3

kubectl delete service/mysql -n lab3

kubectl apply -f sql-dep.yaml 
kubectl apply -f mysql-sv.yaml
kubectl apply -f app-dep-pvc.yaml
kubectl apply -f app-sv.yaml

eksctl delete cluster --name clo835 --region us-east-1
