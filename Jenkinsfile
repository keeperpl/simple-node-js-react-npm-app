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
                npm_config_cache=npm-cache
                ls -l
                pwd
                npm install
                ls -l
                ''' 
            }
        }
    }
}
