# Micro Services WebApp - 6th Semester Cloud Computing Project

Microservices are an architectural and organizational approach to software development where software is composed of small independent services that communicate over well-defined APIs. Microservices architectures make applications easier to scale and faster to develop, enabling innovation and accelerating time-to-market for new features. Docker and Kubernetes are almost synonymous to 'microservices' as they help package and manage the different components of a project/ application, thereby easing up the implementation of a microservices architecture.

In this project, we work with Docker and Kubernetes to make an easily deployable and portable blogging web-app using Flask and MongoDB.

The microservices architecture will deploy a Kubernetes cluster with a mongodb server pod fronted with a web admin interface and a pod to run the flask app.

# Pre-Requisites/ Pre-Installation:
1. Docker
2. Kubernetes

# File Structure

The app directory contains all the code pertaining to the flask app. The mongo connection string variables are configured in app.py

The flask-app-image.dockerfile specifies the insructions to assemble the docker image for the flask app.

The .yaml files in the root directory specify the kubernetes manifests that will bring up your microservices deployment of the problem statement.

# Execution Commands

docker build . -f flask-app-image.dockerfile -t blogapp:1.0

kubectl apply -f secret.yaml

kubectl apply -f configmap.yaml

kubectl apply -f services.yaml

kubectl apply -f deployments.yaml

kubectl get pod


localhost:5001

localhost:8081

# Acknowledgements

I'd like to thank Prof. Saritha and the TAs - Sathvik Saya and Aniket - for their guidance throughout the project. I'd also like to thank my teammates - Tankala Sunaina, U Suchithra and Vivek S D for their contribution in the project.
