pipeline {
  agent any
  tools {
    maven 'apache-maven-3.5.0'
  }
  stages {
    stage('Build') {
      steps {
        sh 'mvn --version'
      }
    }
  }
}
