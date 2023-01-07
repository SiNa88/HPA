# HPA
Walkthrough of HorizontalPodAutoscaler in Kubernetes

## Configuring horizontal Pod autoscaling

This repository is a local test based on the commands in [GKE](https://cloud.google.com/kubernetes-engine/docs/how-to/horizontal-pod-autoscaling).

* ```nano nginx.yaml``` --> [nginx.yaml](https://raw.githubusercontent.com/SiNa88/HPA/main/nginx.yaml)

* ```kubectl apply -f nginx.yaml``` 

* ```nano nginx-hpa.yaml``` --> [nginx-hpa.yaml](https://raw.githubusercontent.com/SiNa88/HPA/main/nginx-hpa.yaml)

* ```kubectl apply -f nginx-hpa.yaml``` 

* ```kubectl get hpa```

  * ```NAME    REFERENCE          TARGETS         MINPODS   MAXPODS   REPLICAS   AGE```

  * ```nginx   Deployment/nginx   <unknown>/50%   1         10        3          19h```

* ```kubectl get hpa nginx -o yaml```

* Download the project under this repository: [Flask](https://github.com/SiNa88/flask_k8s).

* ```python3.9 updateDeployment.py```
