pipeline {
  agent any
  stages {
    stage('Buzz') {
      steps {
        echo 'Buzz Buzz'
      }
    }

    stage('error') {
      agent any
      steps {
        echo 'Its working'
      }
    }

    stage('Sleep') {
      steps {
        sleep 5
        echo 'Sucess'
      }
    }

  }
}