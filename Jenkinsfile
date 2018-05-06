pipeline {
    agent {
        docker {
            image 'node:9' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh '''
                npm --version
                node --version
                npm install --unsafe-perm=true --allow-root
                ''' 
            }
        }
    }
}
