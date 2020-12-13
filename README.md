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


