pipeline {
    agent any // Tells Jenkins to allocate any available runner/agent to execute this pipeline

    stages {
        stage('Build') {
            steps {
                echo 'Compiling the code...'
            }
        }
        stage('Test') {
            steps {
                echo 'Running unit tests...'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying to staging environment...'
            }
        }
    }
}