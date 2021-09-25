pipeline {
    agent any
    stages {
        stage('Deploy') {
            steps {
                nodejs(nodeJSInstallationName: 'nodejs') {
                    withAWS(credentials: 'AWS-POC') {
                        sh 'npm install'
                        sh 'serverless deploy'
                    }
                }
            }
        }
    }
}
