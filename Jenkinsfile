pipeline {
    agent {
        docker {
            image 'node:9-alpine' 
            args '-v ~/.npm:/.npm'
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh '''
                npm install
                ''' 
            }
        }
    }
}
