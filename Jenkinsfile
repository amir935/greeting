pipeline
{
agent any

stages {
     stage('Build Application'){
          steps{
          
                  bat 'mvn  install'
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
  
