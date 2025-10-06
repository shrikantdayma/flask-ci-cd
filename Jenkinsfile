pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/shrikantdayma/flask-ci-cd.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t flask-cicd-app .'
            }
        }
        stage('Run Container') {
            steps {
                sh 'docker run -d -p 5000:5000 --name flask-app flask-cicd-app'
            }
        }
    }
}

