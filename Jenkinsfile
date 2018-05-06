pipeline {
    agent {
        docker {
            image 'node:9-alpine' 
            args "-u root"
        }
    }
    stages {
        stage('Build') { 
                withEnv([
        /* Override the npm cache directory to avoid: EACCES: permission denied, mkdir '/.npm' */
        'npm_config_cache=npm-cache',
        /* set home to our current directory because other bower
        * nonsense breaks with HOME=/, e.g.:
        * EACCES: permission denied, mkdir '/.config'
        */
        'HOME=.',
    ]) 
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
