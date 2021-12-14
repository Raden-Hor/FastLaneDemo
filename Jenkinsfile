pipeline {
  agent any
  stages {
    stage('Setup') {
      steps {
        echo "Setup"
        sh "ls -l"
        sh "pwd"
        // Install fastlane
        sh "brew install fastlane"
        sh "cd android"
        sh "bundle exec fastlane beta"
      }
    }
  }
}
