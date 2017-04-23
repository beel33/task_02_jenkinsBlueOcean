pipeline {
  agent {
    docker 'ruby:2.3.3'
  }
  stages {
    stage('commit-stage') {
      steps {
        sh 'bundle install'
        sh 'rspec'
      }
    }
    stage('security-check-stage') {
      steps {
        sh 'bundle install'
        sh 'bundle exec brakeman -z'
      }
    }
  }
}