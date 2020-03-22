pipeline {
  agent any
  
  stages {
    stage('Build') {
      steps {
        echo 'Building...'
      
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
