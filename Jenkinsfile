

pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                    checkout scm
            }
        }
        stage('Deploy') {
            environment {
                SSH_PRIVATE_KEY = credentials('ssh-private-key')
                REMOTE_HOST = 'ec2-user@13.127.246.18'
                REMOTE_DIR = '/var/www/html'
            }
            steps {
                withCredentials([sshUserPrivateKey(credentialsId: 'ssh-private-key', keyFileVariable: 'SSH_PRIVATE_KEY')]) {
                    sh "scp -i ${SSH_PRIVATE_KEY} -o StrictHostKeyChecking=no -r ${WORKSPACE}/code ${REMOTE_HOST}:${REMOTE_DIR}"
                }
            }
        }
    }
}


