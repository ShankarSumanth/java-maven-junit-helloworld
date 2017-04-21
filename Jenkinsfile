pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        tool(name: 'M3', type: 'maven')
        sh 'M3/bin/mvn --version'
      }
    }
  }
}
