pipeline {
    agent {
        docker {
            image 'node:9-alpine' 
            args "-u root"
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
