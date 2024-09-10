pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                sh '''
                    docker build -t webapp:v1 .
                '''
            }
        }
        stage('Run Docker Container') {
            steps {
                sh '''
                    docker run -d -p 5000:5000 --name web-app-container webapp:v1
                '''
            }
        }
        stage('Test') {
            steps {
                sh '''
                    sleep 5
                    curl -f http://localhost:5000 || exit 1
                '''
            }
        }
        stage('Cleanup') {
            steps {
                sh '''
                    docker stop web-app-container
                    docker rm web-app-container
                '''
            }
        }
    }
}
