
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
                sh 'ssh -i "mahima.pem" ubuntu@ec2-13-127-246-18.ap-south-1.compute.amazonaws.com "cd /var/www/html && git pull"'
            }
        }
    }
}


