pipeline {
  agent any
  
  stages {
    stage('Build') {
      steps {
        echo 'Building...'
        env.totalCommits++
        echo env.totalCommits
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
