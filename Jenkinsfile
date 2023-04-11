

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
                sh "scp -i ${env.EC2_INSTANCE_SSH_KEY} /home/ubuntu ${env.EC2_INSTANCE_USERNAME}@${env.EC2_INSTANCE_IP}:/home/ubuntu"
                sh "ssh -i ${env.EC2_INSTANCE_SSH_KEY} ${env.EC2_INSTANCE_USERNAME}@${env.EC2_INSTANCE_IP} sudo service nginx restart"
            }
        }
    }
}
