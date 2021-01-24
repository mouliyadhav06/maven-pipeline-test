pipeline 
{
    agent any
    stages 
    {
        stage('code-checkout') 
        {
            steps 
            { 
               sh "rm -rf maven-pipeline-test"
                
            }
        }
        
        stage('clean & Test') 
        {
            steps 
            {
                sh "mvn clean"
                sh "mvn test"
                
            }
        }
        
         stage('Deploy') 
        {
            steps 
            {
                sh "mvn package"
            }
        }
        
          stage('Archiving') 
        {
            steps 
            {
                archiveArtifacts '**/target/*.jar'
            }
        }
        
        
        
    }
} 
