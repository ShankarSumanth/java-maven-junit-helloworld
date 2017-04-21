pipeline {
  agent any
  stages {
    stage('Tools') {
      steps {
        echo 'Start Build'
      }
    }
    stage('Preparation') {
      steps {
        git 'https://github.com/ShankarSumanth/java-maven-junit-helloworld.git'
      }
    }
    stage('Build') {
      steps {
        tool name: 'M3', type: 'maven'
        sh '"\'M3/bin/mvn\' -Dmaven.test.failure.ignore clean package"'
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
