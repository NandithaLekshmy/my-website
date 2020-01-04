pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sleep 20
        echo 'Success!'
        archiveArtifacts(artifacts: 'target/*.jar', fingerprint: true, allowEmptyArchive: true)
      }
    }
    stage('Test') {
      steps {
        echo 'Another message'
        junit(testResults: '**/surefire-reports/**/*.xml', allowEmptyResults: true)
      }
    }
  }
  environment {
    Buzz_name = 'Worker bee'
  }
}