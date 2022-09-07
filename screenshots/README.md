# Screenshots
To help review your infrastructure, please include the following screenshots in this directory::
![DockerHub](dockerHub-repo.png)

## Deployment Pipeline
* DockerHub showing containers that you have pushed
* GitHub repository’s settings showing your Travis webhook (can be found in Settings - Webhook)
* Travis CI showing a successful build and deploy job
Payment for travis CI uses stripe api which is not yet supported in my country as a result I used CircleCI instead.
![CircleCI success](circleCI-successful-build.png)

## Kubernetes
* To verify Kubernetes pods are deployed properly
```bash
kubectl get pods
```
![getpods](kubectl-get-pods-screenshots.png)
* To verify Kubernetes services are properly set up
```bash
kubectl describe services
```
![kubectl describe services outputs](describeService-01.png)
![kubectl describe services outputs](describeService-02.png)
![kubectl describe services outputs](describeService-03.png)
![kubectl describe services outputs](describeService-04.png)
![kubectl describe services outputs](describeService-05.png)
* To verify that you have horizontal scaling set against CPU usage
```bash
kubectl describe hpa
```
![kubectl describe hpa outputs](describe-hpa-01.png)
![kubectl describe hpa outputs](describe-hpa-02.png)
![kubectl describe hpa outputs](describe-hpa-03.png)
* To verify that you have set up logging with a backend application
```bash
kubectl logs {pod_name}
```
![frontend logs](01-frontend-logs-sreenshots.png)
![frontend logs](02-frontend-logs-sreenshots.png)
![backend feeds logs](backend-feed-logs-sreenshots.png)
![backend users logs](backend-user-logs-sreenshots.png)
![reverse proxy logs](reverseproxy-logs-sreenshots.png)