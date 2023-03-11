pipeline
{
agent any

stages {
     stage('Build') {
      steps {
        
          bat  mvn -B clean install
          
        
      }
 
     stage('test  application'){
          steps{
                 bat 'mvn test'
            }      
     }

     stage('deploy application to cloudhub'){
     
          steps {
                   bat 'mvn package deploy -DmuleDeploy'
                    }           
          }
      }
}
  
