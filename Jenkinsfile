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
                npm -g config set user root
                npm install
                ''' 
            }
        }
    }
}
