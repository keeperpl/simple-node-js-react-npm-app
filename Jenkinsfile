pipeline {
    agent {
        docker {
            image 'node:9-alpine' 
            args "-u root"
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh '''
                HOME=.
                CI=true
                npm install
                #npm run test > report.xml 2>&1
                echo "aaaa" > report.xml
                cat report.xml
                echo "Test Report \n BUILD_NUMBER: $BUILD_NUMBER " > index.html
                ''' 
            }
            post {
                always {
                    publishHTML([allowMissing: false, alwaysLinkToLastBuild: false, keepAll: true, reportDir: '.', reportFiles: 'index.html', reportName: 'HTMLReport', reportTitles: 'Rep'])
                }
            }
        }
    }
}
