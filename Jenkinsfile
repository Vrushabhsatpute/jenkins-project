// Testing webhook trigger - change 1
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Step 1: Building the app...'
                bat 'dir'
            }
        }

        stage('Test') {
            steps {
                echo 'Step 2: Running tests...'
                echo 'All tests passed!'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Step 3: Deploying to server...'
                echo 'Deployed successfully!'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
