pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}

post 
{
  
  always
  {
    emailext body: 'Summary' , subject: 'pipeline Status' , to: 'mahijasoria@gmail.com'
      }
  }

}





