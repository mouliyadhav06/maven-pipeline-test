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
                sh "mvn clean -f maven-pipeline-test"
                sh "mvn test -f maven-pipeline-test"
                
            }
        }
        
         stage('Deploy') 
        {
            steps 
            {
                sh "mvn package -f maven-pipeline-test"
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
