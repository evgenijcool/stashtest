pipeline {
  agent {
	node {
          label 'test'
     	}
  }
  stages {
    stage('git') {
      steps {
        echo 'git'
        echo 'next git'
	      checkout scm
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
