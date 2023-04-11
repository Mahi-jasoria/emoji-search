
pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                    sudo npm install  
                    sudo npm run build
            }
        }
        stage('Deploy') {
            steps {
                  sh 'scp -r build/* ubuntu@ 13.127.246.18:/var/www/html'
            }
        }
    }
}


