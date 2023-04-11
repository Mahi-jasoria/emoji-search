pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('build code') {
            steps {
                sshagent(['deploy_user']) {
                   sh "scp -o StrictHostKeyChecking=no   /var/jenkins_home/workspace/poc/   ubuntu@13.127.246.18:/var/www/html"
                   
            }
        }
    }
}
}
