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
        stage("Run Deploy"){
            steps{
                script {
                    input message: 'Approve deployment?', ok 'Deploy'
                    //Add actions here
                    echo "Deploy"
                }
            }
        }
    }
}