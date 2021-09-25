pipeline {
    agent any
    stages {
        stage('TestLambda') {
            steps {
                nodejs(nodeJSInstallationName: 'nodejs') {
                    withAWS(credentials: 'AWS-POC') {
                        sh '''
                            
                            integracion/scriptcreds.sh

                        '''
                    }
                }
            }
        }
    }
}