# kubectl 명령어
# 1. kubectl get deploy,rs,po,ep,svc -o wide --show-labels
# 2. kubectl get node
# 3. kubectl create -f *.yaml
# deploy replicas 생성
kubectl create deploy example --image nginx --replicas 3

# label 활용 Cluster resource 조회 관리
kubectl get no --show-labels

# node selector
kubectl label no master1 disktype=~~

# pod 다 지우기
kubelctl delete po --all

# service edit
kubectl edit svc "name"
selector <app> --> "name_2"

#docker hub upload
docker login
docker build -t userID/NAME:TAG
docker push userID/NAME:TAG

adj svc selector
kubectl set selector svc app(svcName) app=greeb
