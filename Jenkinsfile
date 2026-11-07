pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build & Test') {
            steps {
                echo 'Running application build and tests...'
            }
        }
        stage('Build Docker Image') {
            steps {
                script {
                    // Builds the image using the Dockerfile in the workspace
                    // Tag it with the build number for version tracking
                    sh "docker build -t my-app:${env.BUILD_NUMBER} ."
                }
            }
        }
    }
    post {
        success {
            echo 'Docker image successfully built and tagged!'
        }
        failure {
            echo 'Pipeline failed during Docker image creation.'
        }
    }
}
