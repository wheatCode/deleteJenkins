pipeline {
  agent any
  stages { 
        stage('Deploy') {
          steps {

              sh 'mkdir -p frontend'
              script{
                zip zipFile: 'frontend.zip', archive: false, dir: 'frontend'
              }
              sh 'ls -al'
            }
          }
        }
  }
    post {
      always {
          archiveArtifacts artifacts: 'frontend.zip', fingerprint: true
      }
  }
