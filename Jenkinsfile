pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Installing dependencies and compiling...'
                sh 'mvn clean compile'
            }
        }

        stage('Test') {
            steps {
                echo 'Running unit tests...'
                sh 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                sh 'docker run -d --name myapp nginx'
            }
        }
    }
}