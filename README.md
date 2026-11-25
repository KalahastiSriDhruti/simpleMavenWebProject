# Kubernetes Nginx Deployment using Minikube

## 📌 Project Description
This project demonstrates how to deploy an Nginx web server using Kubernetes and expose it to external access through a NodePort Service.

## 🛠️ Technologies Used
- Kubernetes
- Minikube
- kubectl
- Docker
- Nginx

## 🚀 Implementation Steps

### 1. Start Minikube
```bash
minikube start
```

### 2. Create Nginx Deployment
```bash
kubectl create deployment mynginx --image=nginx
```

### 3. Expose Deployment
```bash
kubectl expose deployment mynginx --type=NodePort --port=80 --target-port=80
```

### 4. Check Deployment and Services
```bash
kubectl get deployments
kubectl get pods
kubectl get services
```

### 5. Access the Application
```bash
minikube service mynginx
```

This opens the Nginx web server in the browser.

## 📷 Output
The Nginx welcome page is displayed in the browser, indicating that the deployment and service are working successfully.

## 🎯 Learning Outcomes
- Understanding Kubernetes deployments.
- Creating and managing pods.
- Exposing applications using NodePort Services.
- Deploying containerized applications using Minikube.
- Accessing applications running inside a Kubernetes cluster.

## 👩‍💻 Author
Sri Dhruti

FROM tomcat:9-jdk17-temurin
COPY target/*.war /usr/local/tomcat/webapps/ROOT.war
EXPOSE 8080
CMD ["catalina.sh", "run"]
