# demoArgoCD



docker start argo-test-control-plane

kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d

kubectl apply -f application.yaml

kubectl port-forward svc/argocd-server -n argocd 8443:443 &
kubectl port-forward -n wordpress svc/wordpress 8080:80 &


