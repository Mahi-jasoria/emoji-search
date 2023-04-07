pipeline 
{
    agent any

    stages 
    {
        stage('build')
        {
            steps
            {
                echo 'build test'
                
            }    
                
         }  
         
         
        stage('test')
        {
            steps
            {
                echo 'testing'
            }
            
        }    
                
                
                 
        stage('deployment')
        {
            steps
            {
                sh '''
                #!/bin/bash
                    echo 'deploy'
                    pwd
                '''
                
              
                 
                
                
                
            }    
                
        }        
                
                
                
    }                         
                
                
    post
    {
        
        always
        {
            emailext body: 'summary', subject: 'pipeline status', to: 'mahijasoria@gmail.com'
        }
    }                
}            
            




