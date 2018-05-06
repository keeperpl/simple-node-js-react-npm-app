pipeline {
    agent {
        docker {
            image 'node:9' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh '''
                npm --version
                node --version
                cd $(npm root -g)/npm \
                && npm install fs-extra \
                && sed -i -e s/graceful-fs/fs-extra/ -e s/fs.rename/fs.move/ ./lib/utils/rename.js
                #npm install
                ''' 
            }
        }
    }
}
