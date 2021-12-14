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
        sh "npm install"
        dir('android') {
          sh "ls -l"
          sh "fastlane beta"
        }
      }
    }
  }
}
