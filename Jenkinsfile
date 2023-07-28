pipeline {
  agent any
  stages {
    stage('Buzz') {
      steps {
        echo 'Buzz Buzz'
      }
    }

    stage('Build') {
      steps {
        sh './jenkins/build.sh'
      }
    }

  }
}