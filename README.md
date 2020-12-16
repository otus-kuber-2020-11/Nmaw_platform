# Nmaw_platform
Nmaw Platform repository
00. Prepare git repo
01. Install and run kind and minikube
02. Install pluggin Dashboard for minikube
03. Analize restore pods after delete in namespace kube-system: 
    - coredns(Controlled By:  ReplicaSet) - kubectl describe pods coredns -n kube-system
    - kube-proxy (Controlled By:  DaemonSet/kube-proxy) - kubectl get daemonset.app -n kube-system
    - kube-apiserver and others pods (Controlled By:  Node/minikube)
04. Create Dockerfile and run on local host
05. Create manifest web-pod.yaml and check describe it
06. Add init container to web-pod.yaml manifest
07. Add volumeMounts and volumes to web-pod.yaml manifest
08. Check run web app by kubectl port-forward --address 0.0.0.0 pod/web 8000:8000
09. Clone git repo from Hipster shop, build docker image and push to dockerhub
10. Run container by 'kubectl run frontend --image nmaw/hipster-frontend:v0.0.1 --restart=Never'
11. Get manifest 'kubectl run frontend --image avtandilko/hipster-frontend:v0.0.1 --restart=Never --dry-run=client -o yaml > frontend-pod.yaml'
12. Fix manifest frontend-pod.yaml and add to git branch kubernetes-intro.

HW-2
00. Create kind clister with 3 master nodes and 3 workers nodes
01. Fix frontend-replicaset.yaml and set replicas 3
02. ReplicaSet don`t update pods
03. Prepare paymentservice-replicaset.yaml as frontend-replicaset.yaml
04. Prepare paymentservice-deployment.yaml
05. Update paymentservice-deployment.yaml to v0.0.2
06. Rollout paymentservice-deployment.yaml to v0.0.1
07. Create paymentservice-deployment-bg.yaml for blue green deployment
08. Create paymentservice-deployment-reverse.yaml for Reverse Rolling Update
09. Update frontend-deployment.yaml for use readinessProbe
10. Create node-exporter-daemonset.yaml
11. Update node-exporter-daemonset.yaml for use in all nodes include master nodes

