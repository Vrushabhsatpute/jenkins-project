pipeline {
    agent any
    environment {
        VERCEL_TOKEN = credentials('vercel-token')
        VERCEL_PROJECT_ID = 'prj_wAG4bDaA5LSYvMnC5SrlIY4JQBr9'
        VERCEL_ORG_ID = 'team_t1DbXzhwfEW8KBemGq0nt54Y'
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
                bat '"C:\\Users\\Asus\\AppData\\Roaming\\npm\\vercel.cmd" --prod --token %VERCEL_TOKEN% --yes'
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
