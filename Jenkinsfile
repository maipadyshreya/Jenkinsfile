pipeline {
    agent {
        docker {
            image 'python:3.12.6-alpine3.20'
            args '-u root'
        }
    }
    stages {
        stage('Install dependencies') {
            steps {
                sh '''
                    apk add --no-cache gcc musl-dev python3-dev libffi-dev
                    pip install --upgrade pip
                '''
            }
        }
        stage('Build') {
            steps {
                sh 'python --version'
            }
        }
    }
}
