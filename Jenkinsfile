pipeline
{
agent any

stages {
     stage('Build Application'){
          steps{
          
                  bat 'mvn clean install -Dusername=$ANYPOINT_USERNAME -Dpassword=$ANYPOINT_PASSWORD'
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
  
