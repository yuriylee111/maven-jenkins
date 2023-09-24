pipeline {
  agent any
  options {
    // only keep 10 logs for no more than 10 days
    buildDiscarder(logRotator(daysToKeepStr: '10', numToKeepStr: '10'))

    // cause the build to time out if it runs for more than 12 hours
    timeout(time: 12, unit: 'HOURS')

    // add timestamps to the log
    timestamps()
  }
  triggers {
    cron '@midnight'
  }
  stages {
    stage('pre-build') {
      steps {
        echo 'pre-build'
      }
    }

    stage('build') {
      steps {
        echo 'build'
        build 'maven-project'
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
