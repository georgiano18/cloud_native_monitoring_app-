# Cloud Native Monitoring App

## Overview
This project is a Cloud Native Monitoring application developed using Python and Flask. The application monitors CPU and memory usage and provides alerts if utilization exceeds predefined thresholds. The application is containerized using Docker, deployed to Amazon Elastic Container Registry (ECR), and run on an Amazon Elastic Kubernetes Service (EKS) cluster.

## Features
- Monitors CPU and memory utilization using the `psutil` library.
- Provides alerts for high resource utilization.
- Containerized with Docker for easy deployment.
- Deployed on EKS for scalable and reliable service.
- Configured Kubernetes deployments and services for the application.
- Port forwarding to expose the application for external access.

## Architecture
The application is designed with a microservices architecture, leveraging AWS services and Kubernetes for orchestration. 


## Getting Started

### Prerequisites
- Python 3.x
- Docker
- AWS CLI
- kubectl (Kubernetes CLI)

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/georgiano18/cloud_native_monitoring_app.git
   cd cloud_native_monitoring_app

2. Install the required Python packages:

pip install -r requirements.txt

Running the Application Locally

1. Start the application:
 
python app.py

2. Access the application at http://localhost:5000.
 
Dockerization

1. Build the Docker image:

docker build -t my-flask-app .

2. Run the Docker container:

docker run -p 5000:5000 my-flask-app

Deploying to ECR
1. Authenticate with ECR:

aws ecr get-login-password --region your-region | docker login --username AWS --password-stdin your-account-id.dkr.ecr.your-region.amazonaws.com

2. Tag the Docker image:

docker tag my-flask-app:latest your-account-id.dkr.ecr.your-region.amazonaws.com/my-cloud-native-repo:latest

3. Push the image to ECR:

docker push your-account-id.dkr.ecr.your-region.amazonaws.com/my-cloud-native-repo:latest

Deploying to EKS

1. Create the EKS cluster and nodes.
2. Apply the Kubernetes deployment:
   
kubectl apply -f eks.py

3. Expose the service:

kubectl port-forward service/my-flask-service 5000:5000

License

This project is licensed under the MIT License - see the LICENSE file for details.

Acknowledgements

-Flask for the web framework.
-Docker for containerization.
-AWS for cloud services.
-Kubernetes for orchestration.


