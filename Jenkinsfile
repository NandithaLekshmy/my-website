pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            sleep 20
            echo 'Success!'
            archiveArtifacts(artifacts: 'target/*.jar', fingerprint: true, allowEmptyArchive: true)
            echo 'I am a ${Buzz_name}'
          }
        }
        stage('Build 2') {
          steps {
            echo 'Hey!!'
          }
        }
      }
    }
    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'Another message'
            junit(testResults: '**/surefire-reports/**/*.xml', allowEmptyResults: true)
          }
        }
        stage('Test 2') {
          steps {
            echo 'Hey everyone!!!'
          }
        }
      }
    }
  }
  environment {
    Buzz_name = 'Worker bee'
  }
}