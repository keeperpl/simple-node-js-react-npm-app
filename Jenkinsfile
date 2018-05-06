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
                sudo chown -R $USER:$(id -gn $USER) /.config
                npm install
                ''' 
            }
        }
    }
}
