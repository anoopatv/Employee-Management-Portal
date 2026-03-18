pipeline {
    agent any

    stages {

        stage('Clone Code') {
            steps {
                git 'https://github.com/anoopatv/Employee-Management-Portal.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t todo-app .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 3000:3000 todo-app || true'
            }
        }
    }
}
