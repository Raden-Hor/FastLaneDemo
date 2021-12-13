pipeline {
  agent any
  stages {
    stage('Setup') {
      steps {
        echo "Setup"
        sh "ls -l"
        sh "pwd"
        // Install bundler in order to use fastlane
        sh "gem install bundler"
        // set the local path for bundles in vendor/bundle
        sh "bundle config set --local path 'vendor/bundle'"
        // install bundles if they're not installed
        sh "bundle check || bundle install --jobs=4 --retry=3"
        sh "cd android"
        sh "bundle exec fastlane beta"
      }
    }
  }
}
