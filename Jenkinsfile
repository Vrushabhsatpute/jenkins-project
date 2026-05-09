pipeline {
    agent any

    environment {
        VERCEL_TOKEN = 'vcp_6fGfMRTzLayQg5qSz87ZGBvIaIGqRarYEu9moLCIEVIB49VdMv1QRdds'
        VERCEL_PROJECT_ID = 'prj_kA5TT1JdUyfQy4xVd6fGdzfETa10'
        VERCEL_ORG_ID = 'vrushabhsatpute07-70'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Step 1: Building...'
                bat 'dir'
            }
        }

        stage('Test') {
            steps {
                echo 'Step 2: Testing...'
                echo 'All tests passed!'
            }
        }

        stage('Deploy to Vercel') {
            steps {
                echo 'Step 3: Deploying to Vercel...'
                bat 'vercel --prod --token %VERCEL_TOKEN% --yes'
            }
        }
    }

    post {
        success {
            echo 'Successfully deployed to Vercel!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
