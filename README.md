# HPA
HorizontalPodAutoscaler Walkthrough

## Configuring horizontal Pod autoscaling

* ```nano nginx.yaml```

* ```kubectl apply -f nginx.yaml``` [nginx.yaml](https://raw.githubusercontent.com/SiNa88/HPA/main/nginx.yaml)

* ```nano nginx-hpa.yaml```

* ```kubectl apply -f nginx-hpa.yaml``` [nginx-hpa.yaml](https://raw.githubusercontent.com/SiNa88/HPA/main/nginx-hpa.yaml)

* ```kubectl get hpa```

  * ```NAME    REFERENCE          TARGETS         MINPODS   MAXPODS   REPLICAS   AGE```

  * ```nginx   Deployment/nginx   <unknown>/50%   1         10        3          19h```

* ```kubectl get hpa nginx -o yaml```
