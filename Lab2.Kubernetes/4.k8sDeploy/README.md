# Kubernetes Deploy Workshop :
* ./Lab1.Kubespray/1.KubernetesBasic/README.md 파일을 참고 하여 문제를 푸세요.
* 답은 Solution.md 파일에 있습니다.
## 1. Deployment를 출력하시오.
```
kubectl get deployment
```
## 2. httpd 이미지를 사용하는 h1 Deploy를 생성하시오 (80번 포트 Open)
```
kubectl create deployment --image=httpd --port=80 h1 
```

## 3. h1 deploy의 80번 포트를 Service로 Open하시오.
```
kubectl expose deployment h1 --type="nodePort" -port 80 
```

## 4. h1 deploy의 복제 갯수를 3으로 늘리시오.
```
kubectl scale deployment h1 --replicas=3 
```

## 5. 위에서 생성한 모든 deploy,service를 삭제하시오.
```
kubectl delete service/h1
kubectl delete deployment/h1
```
