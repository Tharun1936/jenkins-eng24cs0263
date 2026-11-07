pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building application artifacts...'
            }
        }
        stage('Test') {
            steps {
                echo 'Running automated tests...'
            }
        }
        stage('Package') {
            steps {
                echo 'Packaging application into deployable format...'
            }
        }
    }
    post {
        success {
            echo 'CI/CD Pipeline executed successfully!'
        }
        failure {
            echo 'Pipeline failed during execution.'
        }
    }
}
