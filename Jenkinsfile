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
        // Add some testing code implementation here
      }
    }
    stage ('Package') {
      steps {
        echo 'Packaging...'
        // Add some packaging code implementation here
      }
    }
    stage ('Deploy') {
      when {
        branch 'master'
      }
      steps {
        echo 'Deploying...'
        // Add some deploying code implementation here
      }
    }
  }
}
