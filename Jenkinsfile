pipeline {
  agent any
  stages {
    stage('git') {
      steps {
        echo 'git'
        echo 'next git'
      }
    }
    stage('test') {
      steps {
        echo 'test step1'
        echo 'test step2'
      }
    }
    stage('accept') {
      steps {
        input(message: 'accept publish', id: '1', submitter: 'test', submitterParameter: 'testParam')
      }
    }
  }
}