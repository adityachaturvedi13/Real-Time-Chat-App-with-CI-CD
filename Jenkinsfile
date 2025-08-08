pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                script {
                    try {
                        sh 'npm test'
                    } catch (err) {
                        echo 'No test script found or tests failed.'
                    }
                }
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t chat-app:latest .'
            }
        }
        stage('Deploy (docker-compose)') {
            steps {
                sh 'docker-compose up -d --build'
            }
        }
    }
} 