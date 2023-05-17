
# Screenshots
To help review your infrastructure, please include the following screenshots in this directory::

## Deployment Pipeline
* DockerHub showing containers that you have pushed
![Docker images](https://github.com/ValGrace/udagram-microservices/blob/main/screenshots/images/containers.PNG)

* GitHub repository’s settings showing your Travis webhook (can be found in Settings - Webhook)
* Travis CI showing a successful build and deploy job
![travis ci build](https://github.com/ValGrace/udagram-microservices/blob/main/screenshots/images/travis_ci.PNG)
![travis ci build](https://github.com/ValGrace/udagram-microservices/blob/main/screenshots/images/yfvkvjh.PNG)

## Kubernetes
An AWS Elastic Kubernetes Service Cluster is created using eksctl and kubectl tools having granted the required iam permissions.
Managed node groups are also spinned up inside the cluster which will allow for the automatic creation of ec2 instances that provisions compute capacity for our application.

* To verify Kubernetes pods are deployed properly
```bash
kubectl get pods

```
![pods](https://github.com/ValGrace/udagram-microservices/blob/main/screenshots/images/running-pods.PNG)

* To verify Kubernetes services are properly set up
```bash
kubectl describe services

```
![services](https://github.com/ValGrace/udagram-microservices/blob/main/screenshots/images/services.PNG)

* To verify that you have horizontal scaling set against CPU usage
```bash
kubectl describe hpa

```
![scaling](https://github.com/ValGrace/udagram-microservices/blob/main/screenshots/images/hpa.PNG)

* To verify that you have set up logging with a backend application
```bash
kubectl logs {pod_name}
```
![user logs](https://github.com/ValGrace/udagram-microservices/blob/main/screenshots/images/user-logs.PNG)


