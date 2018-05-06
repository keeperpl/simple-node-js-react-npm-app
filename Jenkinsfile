pipeline {
    agent {
        docker {
            image 'node:9-alpine' 
            args "-u root"
        }
    }
    stages {
        withEnv(['npm_config_cache=npm-cache', 'HOME=.']) 
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
