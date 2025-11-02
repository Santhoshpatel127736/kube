pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                echo 'Getting code from GitHub...'
                git branch: 'main', url: 'https://github.com/Santhoshpatel127736/kube.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                echo 'Building Docker image...'
                sh 'docker build -t kube-app .'
            }
        }

        stage('Run Docker Container') {
            steps {
                echo 'Running Docker container...'
                sh 'docker run -d -p 3000:3000 kube-app'
            }
        }
    }
}

