# cloudT
Nginx install

# Building & Running

Copy the sources to your docker host and build the container, and to run.
```
	docker build --rm -t mimdong/ubuntu .
	docker run -it --name n1 -p 8888:80 mimdong/ubuntu



# Q3. Container deploy by Kubernetes
```
kubectl run nginx10 --image=mimdong/ubunt --port=80
# 명령 실행 결과 -> deployment.apps/nginx10 created

#service port는 20번
kubectl expose deploy/nginx --type="NodePort" --port 80   
# 명령 실행 결과 -> service/nginx10 exposed

#pod는 20개 사용
kubectl scale deploy nginx --replicas=20
# 명령 실행 결과 -> deployment.extensions/nginx10 scaled
#kubectl get po
