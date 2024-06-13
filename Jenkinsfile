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
                    bat 'copy /Y build "D:\\jenkins-projects"'
                }
            }
        }
    }
}