# LangInfra IDE chart

Helm chart for LangInfra as IDE with a persistent storage or an external database (for example PostgreSQL).


## Quick start

Install the chart:

```bash
helm repo add langinfra https://langinfra.github.io/langinfra-helm-charts
helm repo update
helm install langinfra-ide langinfra/langinfra-ide -n langinfra --create-namespace
```


## Examples
See more examples in the [examples directory](https://github.com/langinfra/langinfra-helm-charts/tree/main/examples/langinfra-ide).