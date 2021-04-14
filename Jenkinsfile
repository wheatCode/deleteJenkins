pipeline {
  agent any
  stages { 
        stage('Deploy') {
          steps {
              zip zipFile: 'frontend.zip', archive: true, dir: ''
              sh 'ls -al'
            }
          }
        }
    post {
      always {
          archiveArtifacts artifacts: 'frontend.zip', fingerprint: true
      }
  }      
  }
