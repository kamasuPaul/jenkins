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

    stage('Ask for input') {
      steps {
        input(message: 'Hello, Please confirm the deployment?', id: 'confirm')
      }
    }

    stage('Deployment') {
      steps {
        echo 'Deployment success'
      }
    }

  }
  post {
    always {
      mail(to: 'kamasupaul@sybyl.com', subject: "Finished run for build ${env.BUILD_ID}, commit ${env.GIT_BRANCH} (${env.GIT_COMMIT.substring(0,6)})", body: 'Placheholder')
    }

  }
}