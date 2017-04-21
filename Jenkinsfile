pipeline {
  agent any
  stages {
    stage('Tools') {
      steps {
        echo 'Start Build'
      }
    }
    stage('Checkout') {
      steps{
        checkout scm 
      }
    }
    stage('Build') {
      steps {
        sh 'mvn -Dmaven.test.failure.ignore clean package'
      }
    }
    stage('Results') {
      steps {
        junit '**/target/surefire-reports/TEST-*.xml'
        archive 'target/*.jar'
      }
    }
  }
}
