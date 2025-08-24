**CI/CD with GitHub Actions, Docker & Minikube**

***Steps Followed***

**1. Application Setup**

Created a simple Flask app (app.py) with one test (test_app.py).

Added requirements.txt for dependencies.

***2. Containerization***

Wrote a Dockerfile to containerize the app.

***3. GitHub Actions Workflow***

Created .github/workflows/ci-cd.yml to:

Install dependencies

Run tests with pytest

Build Docker image

Push image to Docker Hub

***4. GitHub Secrets***

DOCKER_USERNAME → Docker Hub username

DOCKER_PASSWORD → Docker Hub password/access token

***5. Deployment with Minikube***

minikube start

kubectl apply -f deployment.yml

kubectl get pods

kubectl get svc

minikube service flask-service