pipeline {
    agent any

    environmet {
        IMAGE_NAME = rsakhamuri/jenkins-flask-app
    }

    stages {
        stage('Checkout') {
            steps {
                echo "Code checkout completed successfully."
            }
        }

        stage('Build Docker image') {
            steps {
                sh 'docker build -t $IMAGE_NAME:latest .'
            }
        }

        stage('docker image info') {
            steps {
                sh 'docker images | grep -i jenkins*'
            }
        }
    }
}