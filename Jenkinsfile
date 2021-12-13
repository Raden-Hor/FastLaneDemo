pipeline {
  agent any
  stages {
    stage('Setup') {
      steps {
        echo "Setup"
        sh "cd android"
        sh "fastlane beta"
      }
    }
  }
}
