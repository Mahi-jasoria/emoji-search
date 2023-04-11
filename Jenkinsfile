

pipeline {
    agent any
    stages {
        steps {
            checkout scm
    }
    stages {
        stage('Deploy code') {
            steps {
                sh "scp -i mahima.pem ubuntu@13.127.246.18:/var/www/html"
            }
        }
    }
}
