pipeline {
  agent any
  stages {
    stage('Tools') {
      steps {
        echo 'Start Build'
      }
    }
   stage('Preparation') { // for display purposes
      // Get some code from a GitHub repository
     steps {
        git 'https://github.com/ShankarSumanth/java-maven-junit-helloworld.git'
        // Get the Maven tool.
        // ** NOTE: This 'M3' Maven tool must be configured
        // **       in the global configuration.           
        tool name: 'M3', type: 'maven' 
     }
   }
   stage('Build') {
      steps {
        // Run the maven build
        //if (isUnix()) {
           sh "'${mvnHome}/bin/mvn' -Dmaven.test.failure.ignore clean package"
        //} else {
        //   bat(/"${mvnHome}\bin\mvn" -Dmaven.test.failure.ignore clean package/)
        //}        
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
