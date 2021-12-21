pipeline {
  agent any
  environment {
    LANG="en_US.UTF-8"
    LANGUAGE="en_US.UTF-8"
    LC_ALL="en_US.UTF-8"
  }
  stages {
    stage('Setup') {
      steps {
        echo "Setup"
        echo 'Pulling...' + env.BRANCH_NAME
        sh "ls -l"
        sh "pwd"
        // Install fastlane
        sh "gem -v"
        sh "docker -v"
        sh "fastlane -v"
        echo "clear node cached"
        sendGoogleChat("This is a _simple_ text message " +
            "with a <https://github.com/mkutz/jenkins-google-chat-notification|link>" +
            "\nand a line break, " +
            "which might be interesting to <users/all> users in the Group.")
//         sh "watchman watch-del-all && rm -rf node_modules && yarn"
//         dir('android') {
//           sh "ls -l"
//           sh "fastlane beta"
//         }
//         dir('ios') {
//           sh "ls -l"
//           sh "rm -rf Pods"
//           sh "rm -rf Podfile.lock"
//           sh "rm -rf ~/Library/Developer/Xcode/DerivedData/*"
//           sh "pod install"
//           sh "fastlane beta"
//         }
      }
    }
  }
}
