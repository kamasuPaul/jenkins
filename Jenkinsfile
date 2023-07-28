pipeline {
  agent any
  stages {
    stage('Buzz') {
      steps {
        echo 'Buzz Buzz'
      }
    }

    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            sh './jenkins/build.sh'
          }
        }

        stage('Print paul') {
          steps {
            echo '$PAUL'
          }
        }

        stage('echo') {
          steps {
            echo 'How are you'
          }
        }

      }
    }

    stage('Finish') {
      steps {
        echo 'Done'
      }
    }

  }
  environment {
    PAUL = 'KAMASU'
  }
}