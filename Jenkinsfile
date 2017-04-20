pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        echo 'Pull From SCM Complete'
      }
    }
    stage('Build') {
      steps {
        bat(script: '%MAVEN_HOME%/bin/mvn clean install', returnStatus: true, returnStdout: true, encoding: 'UTF-8')
      }
    }
  }
}