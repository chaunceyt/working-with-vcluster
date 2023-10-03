# Get argocd password

kubectl get secrets -n argocd argocd-initial-admin-secret -o yaml | grep password: | awk '{print $2}' | base64 -D
