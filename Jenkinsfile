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
                ls -l
                pwd
                npm install
                ls -l
                ''' 
            }
        }
    }
}
