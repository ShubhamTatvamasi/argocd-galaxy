# argocd-galaxy

Install dependant collections:
```bash
ansible-galaxy collection install shubhamtatvamasi.awx
```

Install Argo CD:
```bash
ansible-playbook deploy-agrocd-tls.yml
```
> It takes 10 minutes to start after deployment is done.

ID: `admin`, password:
```bash
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d; echo
```
