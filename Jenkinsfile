pipeline {
  agent any
  
  stages {
    stage('Build') {
      steps {
        sh './mvnw package'
      }
    }
    stage ('Test') {
      steps {
        echo 'Testing...'
      }
    }
    stage ('Package') {
      steps {
        echo 'Packaging...'
      }
    }
    stage ('Deploy') {
      when {
        branch 'master'
      }
      steps {
        echo 'Deploying...'
      }
    }
  }
  post {
    success {
      slackSend (color: '#00FF00', message: "Successful Deploy: Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]'")
    }
  }
}
