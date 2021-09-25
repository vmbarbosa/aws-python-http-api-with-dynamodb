pipeline {
    agent any
    stages {
        stage('TestLambda') {
            steps {
                nodejs(nodeJSInstallationName: 'nodejs') {
                    withAWS(credentials: 'AWS-POC') {
                        sh '''
                            apt-get install jq
                            integracion/scriptcreds.sh

                        '''
                    }
                }
            }
        }
    }
}