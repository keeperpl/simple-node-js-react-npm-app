pipeline {
    agent {
        docker {
            image 'node:9-alpine' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh '''
                HOME=.
                ls -l
                pwd
                npm install
                ls -l
                ''' 
            }
        }
    }
}
