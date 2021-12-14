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
//         echo "clear node cached"
//         sh "watchman watch-del-all && rm -rf node_modules && yarn"
//         dir('android') {
//           sh "ls -l"
//           sh "fastlane beta"
//         }
        dir('ios') {
          sh "ls -l"
          sh "rm -rf Pods"
          sh "rm -rf Podfile.lock"
          sh "rm -rf ~/Library/Developer/Xcode/DerivedData/*"
          sh "pod install"
          sh "fastlane beta"
        }
      }
    }
  }
}
