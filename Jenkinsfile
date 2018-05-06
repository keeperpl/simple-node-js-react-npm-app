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
                echo "Strona raportu testow" > index.html
                ''' 
            }
            post {
                always {
                    junit 'report.xml' 
                    publishHTML([allowMissing: false, alwaysLinkToLastBuild: false, keepAll: false, reportDir: '', reportFiles: 'index.html', reportName: 'HTML Report', reportTitles: ''])
                }
            }
        }
    }
}
