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
                scp -i  key.pem ubuntu@13.127.246.18:/var/www/html 
            }
        }
    }
}
