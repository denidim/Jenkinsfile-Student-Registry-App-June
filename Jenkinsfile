pipeline{
    agent any
    stages{
        stage("NPM Install"){
            steps{
                bat 'npm install'
            }
        }
        stage("Run Audit"){
            steps{
                bat 'npm audit'
            }
        }
        stage("Run Integration Test"){
            steps{
                bat 'npm test'
            }
        }
    }
}