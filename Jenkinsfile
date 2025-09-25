pipeline {
    agent any
    stages {
        stage('Build Docker Image') {
            steps {
                bat 'docker build -t week2 .'
            }
        }
        stage('Push to Docker Hub') {
            steps {
                bat 'docker tag week2 srujanadara/registration:v1'
                bat 'docker push srujanadara/registration:v1'
            }
        }
        stage('Deploy to Kubernetes') {
            steps {
                bat 'kubectl apply -f C:/Users/ASUS/OneDrive/Desktop/Devops/deployment.yaml'
                bat 'kubectl apply -f C:/Users/ASUS/OneDrive/Desktop/Devops/service.yaml'
            }
        }
    }
}
