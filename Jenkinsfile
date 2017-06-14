pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'build'
      }
    }
    stage('error') {
      steps {
        sh '''chmod +x gradlew
./gradlew build'''
      }
    }
  }
}