pipeline {
  agent any
  stages { 
        stage('Deploy') {
          steps {
              // zip dir: "",glob: '',zipFile: "frontend.zip", archive: true
              zip
              sh 'ls -al'
            }
          }
        }
    post {
      always {
          archiveArtifacts artifacts: "frontend.zip", fingerprint: true
      }
  }      
  }
