pipeline {
  agent {
    node {
      label 'agent1'
    }

  }
  stages {
    stage('StartPipeline') {
      steps {
        echo 'Hello, starting pipeline....'
      }
    }

    stage('Run shell') {
      steps {
        sh './jenkins/build.sh'
      }
    }

    stage('Test') {
      steps {
        sh './jenkins/test-all.sh'
      }
    }

  }
}