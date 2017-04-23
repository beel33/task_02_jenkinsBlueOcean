properties([gitLabConnection('git@git.mediacube.at:menow/app.git')])

pipeline {
    agent { docker 'ruby:2.3.3' }
    stages {
        stage('commit-stage') {
            steps {
                sh 'apt-get update -qq && apt-get install -y build-essential nodejs'
                sh 'bundle install'
                sh 'rspec'
            }
        }

        stage('security-check-stage') {
            steps {
                sh 'apt-get update -qq && apt-get install -y build-essential nodejs'
                sh 'bundle install'
                sh 'bundle exec brakeman -z'
            }
        }
    }
}
