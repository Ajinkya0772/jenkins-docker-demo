pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                echo 'Building Docker image...'
                sh 'docker build -t demo-app .'
            }
        }

        stage('Run Container') {
            steps {
                echo 'Running container...'
                sh 'docker run -d -p 8081:80 --name demo-container demo-app || true'
            }
        }
    }
}
