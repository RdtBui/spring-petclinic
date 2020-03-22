node {
    stage('Build') {
     
        echo 'Building...'
      
       

         getLastSuccessfulCommit()
        
        sh './mvnw package'
      
    }
    stage ('Test') {
      
        echo 'Testing...'
      
    }
    stage ('Package') {
      
        echo 'Packaging...'
      
    }
}

def getLastSuccessfulCommit() {
              def lastSuccessfulHash = null
              def lastSuccessfulBuild = currentBuild.getPreviousSuccessfulBuild()

              if ( lastSuccessfulBuild ) {
                  lastSuccessfulHash = commitHashForBuild( lastSuccessfulBuild )
              }
              return lastSuccessfulHash
        }
