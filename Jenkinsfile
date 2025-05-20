pipeline {
    agent any

    stages {
        stage('NPM Install') {
            steps {
                bat 'npm install'
            }
        }

        stage('Run npm audit') {
            steps {
                bat 'npm audit'
            }
        }

        stage('Deploy to STAGING') {
            steps {
                echo 'Deploying to STAGING'
            }
        }

        stage('Approval for PRODUCTION Deployment') {
            steps {
                script {
                    input message: 'Proceed with production deployment?', ok: 'Deploy'
                }
            }
        }

        stage('Deploy to PRODUCTION') {
            steps {
                echo 'Deploying to PRODUCTION'
            }
        }        
    }
}