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
                   sh "scp -o StrictHostKeyChecking=no    /home/ubuntu/workspace/poc ubuntu@13.127.246.18:/home/ubuntu"
                   
            }
        }
    }
}
