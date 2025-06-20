pipeline {
  agent { label 'Jenkins-agent'}
  tools {
    jdk 'java17'
    maven 'Maven3'
  }
  stages{
    stage("Cleanup Workspace"){
           steps {
           cleanWs()
           }
    }
    
  }
    stage("Checkout from Github"){
           steps {
           Git branch: 'main', credentialsId: 'github', url: 'https://github.com/dilli7230/Demo2.git'
           }
    }
    
  
   
    stage("Checkout from Github"){
           steps {
              Git branch: 'main', credentialsId: 'github', url: 'https://github.com/dilli7230/Demo2.git'
           }
    }
     stage("Build Application"){
           steps {
               sh "mvn clean package"
           }
    } 
    stage("test Application"){
           steps {
               sh "mvn test"
           }
    } 
}
