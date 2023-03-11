pipeline
{
agent any

stages {
     stage('Build Application'){
          steps{
          
                  bat 'mvn clean install -U'
        }
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
  
