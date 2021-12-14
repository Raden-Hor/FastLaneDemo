pipeline {
  agent any
  stages {
    stage('Setup') {
      steps {
        echo "Setup"
        sh "ls -l"
        sh "pwd"
        // Install fastlane
        sh "gem -v"
        sh "docker -v"
        sh "fastlane -v"
        dir('android') {
          sh "ls -l"
          sh "fastlane beta"
        }
      }
    }
  }
}
