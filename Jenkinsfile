pipeline {
  agent any 
  stages {
     stage('Build') {
        steps {
           echo 'Hello World'
          sh 'echo "Hello from Jenkins" > output.txt'
        }
     }
  }
  post{
    always {
      archiveArtifacts artifacts: 'output.txt', allowEmptyArchive: false
    }
  }
}
