pipeline {
  agent any
  
  stages {
    stage('Build') {
      steps {
        echo 'Building...'
        
        script {
          if (fileExists('message1.json')) {
            echo 'Exists'
          } else {
            echo 'Don\'t exists'
            def data = readJSON text: '{}'
            data.a = "test: ${myVar}" as String
            writeJSON(file: 'message1.json', json: data, pretty: 4)
          }
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
