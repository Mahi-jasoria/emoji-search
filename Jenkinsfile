

pipeline {
    agent any
    environment {
        EC2_INSTANCE_IP = "13.127.246.18"
        EC2_INSTANCE_USERNAME = "ubuntu"
        EC2_INSTANCE_SSH_KEY = "~/.ssh/knowm_hosts"
    }
    stages {
        stage('Deploy code') {
            steps {
                sh "scp -i mahima.pem ubuntu@13.127.246.18:/var/www/html"
            }
        }
    }
}
