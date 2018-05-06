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
                npm run test > report.xml 2>&1
                ''' 
            }
        }
    }
}
