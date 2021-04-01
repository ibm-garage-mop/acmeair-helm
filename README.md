```
helm install acmeair2 acmeair --set host=acmeair2.apps.ocp4.demointel.mpl --create-namespace -n acmeair2
```

with istio
```
helm install acmeair acmeair --set host=acmeair.apps.ocp-1.sric.kb --set istio.enabled=true --create-namespace -n acmeair
```

with quay plugin 
```
helm plugin install https://github.com/app-registry/quay-helmv3-plugin

helm quay install quay.io/schabrolles/acmeair -- acmeair --set host=acmeair.apps.sandbox.power.mpl --create-namespace -n acmeair
```


