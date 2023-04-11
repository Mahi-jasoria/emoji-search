
pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Deploy') {
            steps {
                  sh 'scp -i ~/. ssh/known_hosts  ubuntu@ 13.127.246.18:/var/www/html'
            }
        }
    }
}


