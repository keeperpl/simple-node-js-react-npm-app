pipeline {
    agent {
        docker {
            image 'iron/node' 
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
