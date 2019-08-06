pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'echo test > testscp.jar'
        sh 'ls'
        sleep 5
        input 'message-test'
      }
    }
    stage('Test') {
      environment {
        CI = 'true'
      }
      steps {
        sh './jenkins/scripts/test.sh'
      }
    }
  }
}