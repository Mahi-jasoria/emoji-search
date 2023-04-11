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
                sh 'scp -i  mahima.pem ubuntu@13.127.246.18"cd/var/www/html"' 
            }
        }
    }
}
