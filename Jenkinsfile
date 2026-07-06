pipeline {
    agent any

    stages {

        stage('Clone') {
            steps {
                git 'https://github.com/YOUR_USERNAME/jenkins-docker-demo.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t jenkins-demo .'
            }
        }

        stage('Run Container') {
            steps {
                bat 'docker run -d -p 5000:5000 --name demo-container jenkins-demo'
            }
        }
    }
}
