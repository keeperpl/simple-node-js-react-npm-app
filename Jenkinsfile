pipeline {
    agent {
        docker {
            image 'node:9-alpine' 
            args '-v /var/lib/jenkins/.npm:/.npm'
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
