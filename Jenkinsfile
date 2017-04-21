pipeline {
  agent any
  tools {
    jdk 'java8'
    maven 'M3'
  }
  stages {
    stage('Build') {
      steps {
        sh 'mvn --version'
      }
    }
  }
}
