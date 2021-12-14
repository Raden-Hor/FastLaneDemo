pipeline {
  agent any
  stages {
    stage('Setup') {
      steps {
        echo "Setup"
        sh "ls -l"
        sh "pwd"
        // Install fastlane
        sh "docker ps"
//         sh "docker exec 48d1bf786499 brew -v"
        sh "cd android"
        sh "bundle exec fastlane beta"
      }
    }
  }
}
