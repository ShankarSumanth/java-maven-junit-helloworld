pipeline {
  agent any
  tools {
    git 'git' 
  }
  stages {
    stage('Build') {
      steps {
        sh 'mvn -Dmaven.test.failure.ignore=true clean package'
      }
    }
  }
}
