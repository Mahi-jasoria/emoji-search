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
                sh 'ssh -i ~/.ssh/known_hosts ubuntu@13.127.246.18 "cd /var/www/html && git pull"'
            }
        }
    }
}
