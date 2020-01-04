pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sleep 20
        echo 'Success!'
        archiveArtifacts(artifacts: 'targets/*.jar', fingerprint: true)
      }
    }
    stage('Test') {
      steps {
        echo 'Another message'
      }
    }
  }
}