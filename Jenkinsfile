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
}
