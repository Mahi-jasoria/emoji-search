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
            




