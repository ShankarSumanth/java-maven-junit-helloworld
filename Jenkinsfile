pipeline {
  agent any
  tools {
    M3 'apache-maven-3.5.0'
  }
  stages {
    stage('Build') {
      steps {
        sh 'mvn --version'
      }
    }
  }
}
