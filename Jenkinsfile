pipeline {
    agent {
        docker {
            image 'appsvc/node' 
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
