pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/harisathar04/simple-reactjs-app.git'
            }
        }
        stage('Dependency Installation') {
            steps {
                sh '/usr/local/bin/npm install'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t i211159_Lab10_11 .'
            }
        }
        stage('Run Docker Image') {
            steps {
                sh 'docker run -d -p 8080:80 i211159_Lab10_11'
            }
        }
        stage('Push Docker Image') {
            steps {
                sh 'docker push i211159_Lab10_11'
            }
        }
    }
}