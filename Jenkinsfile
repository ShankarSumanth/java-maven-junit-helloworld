pipeline {
  agent any
  stages {
    stage('Tools') {
      steps {
        echo 'Pull From SCM'
        tool(name: 'Git', type: 'Git')
      }
    }
  }
}