# Notes


```sh
# build
helm dep update
helm package . -d charts/
# install
helm upgrade --install my-mail .
# install tag
helm upgrade --install my-mail oci://registry-1.docker.io/bpteodor/poste-io:0.4.1
```
