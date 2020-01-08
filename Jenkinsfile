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
    stage('Test') {
         steps {
            sh './jenkins/scripts/test.sh'
            }
     }
    stages {
        stage('Build') { 
            steps {
                sh 'npm install' 
            }
        }
    }
}
