/* Requires the Docker Pipeline plugin */
pipeline {
    agent { docker { image 'python:3.11.1-alpine3.19' } }
    stages {
        stage('build') {
            steps {
                sh 'python --version'
            }
        }
    }
}