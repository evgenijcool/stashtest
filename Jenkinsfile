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
        sh '''PATH=$PATH:$ANDROID_HOME/tools:$ANDROID_HOME/platform-tools
chmod +x gradlew
./gradlew clean'''
      }
    }
  }
}