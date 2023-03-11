pipeline
{
agent any

stages {
     stage('Build') {
      steps {
        withCredentials([usernamePassword(credentialsId: 'd297e15f-eaa9-4c90-847a-c3c82a1d1bd2', usernameVariable: 'Amir122306', passwordVariable: 'Amir122306')]) {
          bat  mvn -B clean install
          
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
  
