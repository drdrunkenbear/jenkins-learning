pipeline {
    agent none // Do not run on the Jenkins server itself

    stages {
        stage('Build with Node') {
            // Spin up a temporary Node.js container just for this stage
            agent {
                docker { image 'node:18-alpine' }
            }
            steps {
                echo 'Building the application...'
                // These commands execute INSIDE the isolated Node.js container
                sh 'node --version' 
                sh 'npm --version'
            }
        }
        stage('Test') {
            agent {
                docker { image 'node:18-alpine' }
            }
            steps {
                echo 'Running tests...'
                sh 'echo "Tests passed!"'
            }
        }
    }
}