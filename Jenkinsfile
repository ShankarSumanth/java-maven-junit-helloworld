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
        mvnHome = tool 'M3'
      }
    }
    stage('Build') {
      steps {
        sh '"\'${mvnHome}/bin/mvn\' -Dmaven.test.failure.ignore clean package"'
      }
    }
    stage('Results') {
      steps {
        junit '**/target/surefire-reports/TEST-*.xml'
        archive 'target/*.jar'
      }
    }
  }
  environment {
    mvnHome = 'M3'
  }
}
