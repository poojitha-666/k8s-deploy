pipeline {
    agent any

    environment {
        KUBECONFIG = 'C:\\Users\\muppa\\.kube\\config' // <-- Update for your system
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/poojitha-666/k8s-deploy.git'
            }
        }

        stage('Deploy to Kubernetes') {
            steps {
                bat 'kubectl apply -f k8s/deployment.yaml'
                bat 'kubectl apply -f k8s/service.yaml'
            }
        }
    }
}
