pipeline {
    agent any

    stages {

        stage('Checkout Code') {
            steps {
                git 'https://github.com/Adept010/jenkins-test-project.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t faizan-nginx .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 8082:80 faizan-nginx'
            }
        }

    }
}