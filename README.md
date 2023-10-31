# poste-io
helm chart for poste-io 

```
helm dep update
helm package . -d charts/
helm upgrade --install my-mail .
```