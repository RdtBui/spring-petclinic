pipeline {
  agent any
  
  stages {
    stage('Build') {
      steps {
        echo 'Building...'
        commitId = sh(returnStdout: true, script: 'git rev-parse HEAD')
        script {
          commitId = sh(returnStdout: true, script: 'git rev-parse HEAD')
        }
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
  }
  
  
}
