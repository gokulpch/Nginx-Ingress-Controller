# Nginx-Ingress-Controller
Ingress Controller - Kubernetes Ingress


# Create Resources

kubectl create -f app-deployment.yaml -f app-service.yaml
kubectl create namespace ingress
kubectl create -f default-backend-deployment.yaml -f default-backend-service.yaml -n=ingress
kubectl create -f default-backend-deployment.yaml -f default-backend-service.yaml -n=ingress
kubectl create -f nginx-ingress-controller-config-map.yaml -n=ingress
kubectl create -f nginx-ingress-controller-roles.yaml -n=ingress
kubectl create -f nginx-ingress-controller-deployment.yaml -n=ingress
kubectl create -f nginx-ingress.yaml -n=ingress
kubectl create -f app-ingress.yaml
kubectl create -f nginx-ingress-controller-service.yaml -n=ingress

# Test

curl http://test.cisco.com:31000/app1
curl http://test.cisco.com:31000/app2
curl http://test.cisco.com:32000/nginx_status
