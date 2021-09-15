pipeline
 {
   agent any
   stages{
     stage('Build Application'){
     steps{
     bat 'mvn clean install'
     }
     }
     stage('Deploy Application to Mulesoft CloudHub'){
     steps{
     bat 'mvn package deploy -DmuleDeploy' 
     }
    }
     stage('Perfrom Regression Testing'){
     steps{
     bat 'C:\\Users\\SHOBHANA\\AppData\\Roaming\\npm\\newman run E:\\postman_collection\\Patient.postman_collection.json --disable-unicode'
     }
    }
    stage('SonarQube Testing'){
    steps{
    bat 'mvn sonar:sonar -Dsonar.sources=src/ -Dsonar.host.url=http://localhost:9000 -Dsonar.login=6d76e3ece11322568edc8add1f71056d0e89f0ea'
    }
   }
    
  }
 }
 