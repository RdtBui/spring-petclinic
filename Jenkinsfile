node {
    stage('Build') {
      steps {
        echo 'Building...'
      
       

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

def getLastSuccessfulCommit() {
              def lastSuccessfulHash = null
              def lastSuccessfulBuild = currentBuild.rawBuild.getPreviousSuccessfulBuild()

              if ( lastSuccessfulBuild ) {
                  lastSuccessfulHash = commitHashForBuild( lastSuccessfulBuild )
              }
              return lastSuccessfulHash
        }
