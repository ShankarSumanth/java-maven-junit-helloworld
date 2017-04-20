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
        sh 'mvn clean install'
      }
    }
  }
}