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
        bat(script: '${mvnHome}/bin/mvn clean install', returnStatus: true, returnStdout: true, encoding: 'UTF-8')
      }
    }
  }
}