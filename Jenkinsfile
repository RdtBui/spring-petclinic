node {
    stage('Build') {
      steps {
        echo 'Building...'
      
       
           def getLastSuccessfulCommit() {
              def lastSuccessfulHash = null
              def lastSuccessfulBuild = currentBuild.rawBuild.getPreviousSuccessfulBuild()

              if ( lastSuccessfulBuild ) {
                  lastSuccessfulHash = commitHashForBuild( lastSuccessfulBuild )
              }
              return lastSuccessfulHash
        }
         getLastSuccessfulCommit()
        
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
