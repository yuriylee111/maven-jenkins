pipeline {
  agent any
  stages {
    stage('pre-build') {
      steps {
        echo 'pre-build'
      }
    }

    stage('build') {
      steps {
        echo 'build'
        build 'maven-jenkins'
      }
    }

    stage('test') {
      steps {
        echo 'test'
      }
    }

    stage('deploy') {
      steps {
        echo 'deploy'
      }
    }

  }
}