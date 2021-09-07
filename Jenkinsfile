pipeline
 {
 agent any
 stages{
  stage('Build Application'){
   steps{
    bat 'mvn clean install'}
   }
  stage('Deploy Application to Mulesoft CloudHub'){
   steps{
    bat 'mvn package deploy -DmuleDeploy' 
    }
   }
  stage('Perfrom Regression Testing'){
   steps{
    bat 'newman run E:\\postman_collection\\Patient.postman_collection.json --diable-unicode'
    
    }
   }
  }
 }
 