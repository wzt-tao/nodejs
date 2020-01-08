pipeline {
    agent {
        docker {
            image 'node:6-alpine' 
            args '-p 3000:3000' 
        }
    }
    environment {
        CI = 'true'
    }
    stages {
        stage('Test') {
            steps {
            sh './jenkins/scripts/test.sh'
            }
     }
        stage('Build') { 
            steps {
                sh 'npm install' 
            }
        }
    }
}
