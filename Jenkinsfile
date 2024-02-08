/* Requires the Docker Pipeline plugin */
pipeline {
    agent { docker { image 'python:3.11.8-alpine3.19' } }

    environment {
        DISABLE_AUTH = 'true'
        DB_ENGINE    = 'sqlite'
    }
    stages {
        stage('Build') {
            steps {
                sh 'python --version'
            }
        }
        stage('Test') {
            steps {
                echo "Database engine is ${DB_ENGINE}"
                echo "DISABLE_AUTH is ${DISABLE_AUTH}"
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploying"
            }
        }
    }

    post {
        // always {
        //     sh 'printenv'
        // }
        success {
            echo "Success"
        }
        unstable {
            echo "Unstable"
        }
        failure {
            echo "Failed :("
        }
    }
}