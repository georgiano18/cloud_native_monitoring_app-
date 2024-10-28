Overview

The Python Monitoring App is a cloud-native application designed to monitor CPU and memory utilization of your system. This project encompasses the full lifecycle of application development, including local development, containerization, deployment on Amazon EKS, and monitoring.


*Key Features*

Local Monitoring: The application runs locally on port 5000, displaying real-time CPU and memory metrics.

Containerization: The app is containerized using Docker, allowing for easy deployment and scalability. A Dockerfile is included to facilitate the building of the Docker image.

ECR Integration: The Docker image is pushed to Amazon Elastic Container Registry (ECR), providing a secure repository for your container images.

EKS Deployment: An Amazon EKS cluster is set up with worker nodes to host the application, ensuring high availability and scalability.

Kubernetes Configuration: Kubernetes deployments and services are created using Python, streamlining the deployment process.

Port Forwarding: The application is exposed via Kubernetes port forwarding, allowing access to the service from the local machine.


*Technologies Used*


Python: The main programming language for developing the application.

Flask: A micro web framework used to build the web application.

Docker: For containerization of the application.

AWS ECR: To store and manage Docker images.

AWS EKS: For orchestrating Docker containers using Kubernetes.

*Contributing*

Feel free to contribute to this project by submitting issues or pull requests. Your feedback and contributions are welcome!
