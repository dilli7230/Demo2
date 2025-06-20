pipeline {
  agent { label 'Jenkins-agent' }

  tools {
    jdk "JAVA_HOME"
    maven "MAVEN_HOME"
  }

  stages {
    stage("Cleanup Workspace") {
      steps {
        cleanWs()
      }
    }

    stage("Checkout from Github") {
      steps {
        git branch: 'main', credentialsId: 'github', url: 'https://github.com/dilli7230/Demo2.git'
      }
    }

    stage("Build Application") {
      steps {
        sh "mvn clean package"
      }
    }

    stage("Test Application") {
      steps {
        sh "mvn test"
      }
    }
  }
}
