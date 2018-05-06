pipeline {
    withEnv(['npm_config_cache=npm-cache', 'HOME=.']) 
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
                ls -l
                pwd
                npm install
                ls -l
                ''' 
            }
        }
    }
}
