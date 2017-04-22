pipeline {
  agent any
  tools {
    git 'Default' 
  }
  stages {
    stage('Build') {
      steps {
        sh 'mvn -Dmaven.test.failure.ignore=true clean package'
      }
    }
  }
}
