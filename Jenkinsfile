pipeline {
  agent any
  stages {
    stage('git') {
      steps {
        echo 'git'
        echo 'next git'
        checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'github', url: 'https://github.com/evgenijcool/stashtest.git']]])

        git(url: 'https://github.com/evgenijcool/stashtest.git', branch: 'master', changelog: true, poll: true)
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
