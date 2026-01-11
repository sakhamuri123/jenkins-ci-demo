pipeline {
    agent any

    environment {
        IMAGE_NAME = "yourdockerhubusername/jenkins-flask-app"
    }

    stages {
        stage('Checkout') {
            steps {
                echo "Code checked out"
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t $IMAGE_NAME:latest .'
            }
        }

        stage('Docker Image Info') {
            steps {
                sh 'docker images | grep jenkins-flask-app'
            }
        }
    }
}
