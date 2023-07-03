pipeline {
    agent any
    tools {node.js "NodeJS"}
    stages {
        stage('Source') {
            steps {
                // Get  code from a GitHub repository
                git 'https://github.com/Rushikaple/estore-admin-dashboard.git'

                // Run npm install
                sh "npm install"

                echo 'Source Stage Finished'
            }
        }

        stage('Test') {
            steps {
                // Run Test Cases
                sh "npm run cypress:run"
                echo 'Test Stage Finished'
            }
        }

        stage('Build') {
            steps {
                // Run ng build command
                sh "npm run ng build"
                echo 'Test Stage Finished'
            }
        }
    }
}
