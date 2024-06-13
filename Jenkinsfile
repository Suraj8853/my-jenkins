pipeline {
    agent any 

    stages {
        stage('Build') {
            steps {
                script {
                    bat 'npm install' // Install dependencies
                    
                }
            }
        }
        stage('Deploy (Local)') {
            steps {
                script {
                    bat 'npm run build' 
                    def deployDir = "D:\\jenkins-proj"

                    // Create the deployment directory if it doesn't exist
                    bat "if not exist ${deployDir} mkdir ${deployDir}"

                    // Copy build folder to the deployment directory
                    bat "xcopy build \"${deployDir}\\build\" /s /e /y /i"
                }
            }
        }
    }
}