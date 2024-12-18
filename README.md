# demo-catalog


apply this in your cluster
```
apiVersion: source.toolkit.fluxcd.io/v1
kind: GitRepository
metadata:
  name: demo-catalog
  namespace: workspace_namespace
  labels:
    kommander.d2iq.io/gitapps-gitrepository-type: catalog
    kommander.d2iq.io/gitrepository-type: catalog
spec:
  interval: 1m0s
  ref:
    branch: main
  timeout: 1m0s
  url: https://github.com/tuxtof/demo-catalog.git
```
