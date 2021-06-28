## Deploying ACMEAIR

```
helm install acmeair2 acmeair --set host=acmeair2.apps.ocp4.demointel.mpl --create-namespace -n acmeair2
```
with: 
 - host: URL to configure as route (http://<host>/acmeair)

### with istio
```
helm install acmeair acmeair --set host=acmeair.apps.ocp-1.sric.kb --set istio.enabled=true --create-namespace -n acmeair
```
with:
  - host: URL to configure as route and ISTIO GATEWAY (http://<host>/acmeair)
  - istio.enabled: true to activate ISTIO


 
 ### Deploying JMETER template

```
helm install acmeair-jmeter acmeair-jmeter -n acmeair --set pipeline.enabled=true --set acmeairJmeterImage=image-registry.openshift-image-registry.svc:5000/acmeair/acmeair-jmeter --set registryTLSverify=false --create-namespace
```
