
# Debug build

````
# Build All:
make build-all

# Build debug binary
CGO_ENABLED=0 GO111MODULE=on go build -gcflags "all=-N -l" -o $GOPATH/src/github.com/prometheus/alertmanager/alertmanager ./cmd/alertmanager/main.go

# Build Docker Image


make docker DOCKER_ARCHS=amd64
docker tag prom/alertmanager-linux-amd64:HEAD reg-dhc.app.corpintra.net/caas/alertmanager:v0.17-dbg
docker push reg-dhc.app.corpintra.net/caas/alertmanager:v0.17-dbg
````