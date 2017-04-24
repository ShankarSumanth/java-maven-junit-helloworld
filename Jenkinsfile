pipeline {
  agent any
  tools {
    java "java1.8"
  }
  stages {
    stage('Build') {
      steps {
        bat 'mvn -Dmaven.test.failure.ignore=true clean package'
      }
    }
  }
}
