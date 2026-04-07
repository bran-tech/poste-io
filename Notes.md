# Notes


```sh
# build
helm dep update # optional if -u

# build
VERSION=0.4.1
helm package . --version $VERSION -d charts/
# push to registry
OCI_SERVER=oci://registry-1.docker.io
DOCKERHUB_USERNAME=
DOCKERHUB_PASSWORD=
helm registry login $OCI_SERVER --username $DOCKERHUB_USERNAME --password $DOCKERHUB_PASSWORD
helm push charts/poste-io-$VERSION.tgz $OCI_SERVER/$DOCKERHUB_USERNAME

# install
helm upgrade --install my-mail charts/poste-io-$VERSION.tgz
# or install tag
helm upgrade --install my-mail oci://registry-1.docker.io/$DOCKERHUB_USERNAME/poste-io:$VERSION
```
