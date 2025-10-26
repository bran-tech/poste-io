# Notes


```sh
# build
helm dep update
helm package . -d charts/
# install
helm upgrade --install my-mail .
```