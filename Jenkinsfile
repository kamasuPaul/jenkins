pipeline {
  agent {
    node {
      label 'agent1'
    }

  }
  stages {
    stage('Buzz') {
      steps {
        echo 'Buzz Buzz'
      }
    }

    stage('Buzz build') {
      steps {
        sh './jenkins/build.sh'
      }
    }

    stage('Buzz test') {
      steps {
        sh './jenkins/test-all.sh'
      }
    }

  }
}