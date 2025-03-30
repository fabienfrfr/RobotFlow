# RobotFlow

An Robotic Arm Control Project with AI

## Introduction

This project aims to control multiple robotic arms using artificial intelligence (AI). It is designed following Domain-Driven Design (DDD) and Test-Driven Development (TDD) principles. The project integrates various technologies to ensure a robust, scalable, and high-performing architecture.

## Technologies Used

- **HuggingFace LeRobot**: AI model for controlling robotic arms.
- **Kubernetes**: Container orchestration for deploying and managing microservices.
- **IoT**: Communication with robotic devices.
- **Postgres**: Relational database for data storage.
- **MinIO**: S3-compatible object storage for large data.
- **Apache Kafka and Flink**: Real-time data stream processing.
- **MLFlow**: Machine learning model lifecycle management.
- **FastAPI**: Framework for creating fast and efficient APIs.
- **Pulumi**: Infrastructure as Code for cloud resource provisioning.
- **Gitlab CI**: Continuous integration for automating tests and deployments.
- **Jira**: Task tracking and project management.
- **PowerBI**: Data visualization and dashboard creation.
- **React**: JavaScript library for building dynamic user interfaces.

## Project Structure

Here is a typical project structure for a production-ready project using DDD and TDD:

```
/robot-control-project
│
├── /src
│   ├── /domain
│   │   ├── /models
│   │   │   └── robot_model.py
│   │   ├── /services
│   │   │   └── robot_service.py
│   │   └── /repositories
│   │       └── robot_repository.py
│   │
│   ├── /application
│   │   ├── /use_cases
│   │   │   └── control_robot_use_case.py
│   │   └── /interfaces
│   │       └── robot_interface.py
│   │
│   ├── /infrastructure
│   │   ├── /persistence
│   │   │   └── postgres_repository.py
│   │   ├── /messaging
│   │   │   └── kafka_producer.py
│   │   └── /storage
│   │       └── minio_client.py
│   │
│   ├── /interfaces
│   │   ├── /api
│   │   │   └── fastapi_app.py
│   │   └── /web
│   │       └── react_app.js
│   │
│   └── /shared
│       ├── /config
│       │   └── config.py
│       └── /utils
│           └── helpers.py
│
├── /tests
│   ├── /unit
│   │   └── test_robot_model.py
│   ├── /integration
│   │   └── test_robot_service.py
│   └── /e2e
│       └── test_robot_control.py
│
├── /deployment
│   ├── /kubernetes
│   │   └── deployment.yaml
│   └── /pulumi
│       └── main.py
│
├── /docs
│   └── README.md
│
├── /ci
│   └── gitlab-ci.yml
│
├── requirements.txt
└── Dockerfile
```


## Installation Instructions

### HuggingFace LeRobot

Install the HuggingFace Transformers library:

```bash
pip install transformers
```

### Kubernetes
Install Minikube for local Kubernetes cluster:

```bash
sudo apt update
sudo apt install minikube
minikube start
```

### IoT
Ensure your IoT devices are configured to communicate with the system.

### Postgres
Install PostgreSQL:

```bash
sudo apt update
sudo apt install postgresql postgresql-contrib
```

### MinIO
Install MinIO server:

```bash
wget https://dl.min.io/server/minio/release/linux-amd64/minio
chmod +x minio
./minio server /data
```

### Apache Kafka and Flink
Install Kafka:

```bash
sudo apt update
sudo apt install default-jre
wget https://downloads.apache.org/kafka/3.0.0/kafka_2.13-3.0.0.tgz
tar -xzf kafka_2.13-3.0.0.tgz
cd kafka_2.13-3.0.0
bin/kafka-server-start.sh config/server.properties
```

Install Apache Flink:

```bash
wget https://archive.apache.org/dist/flink/flink-1.14.5/flink-1.14.5-bin-scala_2.12.tgz
tar -xzf flink-1.14.5-bin-scala_2.12.tgz
cd flink-1.14.5
./bin/start-cluster.sh
```

### MLFlow
Install MLFlow:

```bash
pip install mlflow
```

### FastAPI
Install FastAPI:

```bash
pip install fastapi
```

### Pulumi
Install Pulumi:

```bash
curl -fsSL https://get.pulumi.com | sh
```

### Gitlab CI
Configure GitLab CI with the gitlab-ci.yml file.

### Jira
Set up Jira for project management and task tracking.

### PowerBI
Install PowerBI Desktop for data visualization.

### React
Install Create React App:

```bash
npx create-react-app my-app
cd my-app
npm start
```

## Deployment Instructions
Initial Configuration:

Ensure all dependencies are installed using requirements.txt.
Configure necessary environment variables in /shared/config/config.py.
Deploy with Kubernetes:

Use the Kubernetes configuration files in /deployment/kubernetes to deploy microservices.
CI/CD:

Configure GitLab CI with the gitlab-ci.yml file to automate tests and deployments.
Monitoring and Visualization:

Use PowerBI to create dashboards from data stored in Postgres and MinIO.

## Contribution
Contributions are welcome! Please open an issue or submit a pull request for any improvements or bug fixes.

## License
This project is licensed under the MIT License. See the LICENSE file for details.