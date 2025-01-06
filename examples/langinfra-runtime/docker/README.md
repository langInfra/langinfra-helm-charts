# Package the flow as docker image

You can package the flow as a docker image and refer to it in the chart.

```bash
# Download the flows
wget https://raw.githubusercontent.com/datastax/langinfra-charts/main/examples/flows/basic-prompting-hello-world.json
# Build the docker image locally
docker build -t myuser/langinfra-hello-world:1.0.0 .
# Push the image to DockerHub
docker push myuser/langinfra-hello-world:1.0.0
```

The use the runtime chart to deploy the application:

```bash
helm repo add langinfra https://langinfra.github.io/langinfra-helm-charts
helm repo update
helm install langinfra-runtime langinfra/langinfra-runtime \
    --set "image.repository=myuser/langinfra-hello-world" \
    --set "image.tag=1.0.0"
```
