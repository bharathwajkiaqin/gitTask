pipeline {
  agent any 
  stages {
     stage('Hello') {
        steps {
           echo 'Hello World'
          writeFile file:'output.txt: , text: 'Hello from jenkins'
        }
     }
  }
  post{
    success{
      archiveArtifacts artifacts: 'output.txt', fingerprint:true
    }
  }
}
