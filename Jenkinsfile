pipeline {
    agent any
    
    environment {
        // Define variables for Docker image and container name
        DOCKER_IMAGE = 'yolo:latest'
        DOCKER_CONTAINER_NAME = 'yolo-frontend'
        DOCKER_CONTAINER_NAME = 'yolo-backend'
        DOCKER_CONTAINER_NAME = 'yolo-mongo'
    }

    stages {
        stage('Checkout') {
            steps {
                // Checkout your source code from version control
                checkout scm
            }
        }
        stage('Clone repository') {
            steps {
                // Checkout the repository
                git 'https://github.com/spiral99/yolo.git'
            }
        }
        stage('Deploy') {
            steps {
                // Use Docker Compose to deploy your application
                script {
                    sh 'docker-compose down' // Ensure any previous containers are stopped and removed
                    sh 'docker-compose up -d' // Run containers in the background
                }
            }
        }
    }
}
