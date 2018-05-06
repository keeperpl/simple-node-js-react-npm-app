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
                curl https://raw.githubusercontent.com/creationix/nvm/master/install.sh | sh
                source ~/.nvm/nvm.sh
                nvm install 9.5.0
                nvm use 9.5.0
                npm install
                ''' 
            }
        }
    }
}
