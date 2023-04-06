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
                
                
                 
        stage('deploy')
        {
            steps
            {
                echo 'deploy'
                
                 whoami
                 
                
                
                
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
            




