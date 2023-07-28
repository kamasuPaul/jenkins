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
  post{
    always{
      mail(
        to: 'kamasupaul@sybyl.com', //TODO: add this to env
        subject: "Finished run for build ${env.BUILD_ID}, commit ${env.GIT_BRANCH} (${env.GIT_COMMIT.substring(0,6)})",
        body:'Placheholder'
      )
    }
  }
}