pipeline {
  agent any
  stages {
    stage('Setup') {
      steps {
        echo "Setup"
        sh "ls -l"
        sh "pwd"
        // Install fastlane
        sh "sh /var/jenkins_home/test.sh"
        sh "cd android"
        sh "bundle exec fastlane beta"
      }
    }
  }
}
