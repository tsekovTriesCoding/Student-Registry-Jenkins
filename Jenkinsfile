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

        stage('Deploy to PRODUCTION') {
            steps {
                echo 'Deploying to PRODUCTION'
            }
        }        
    }
}