pipeline {
  agent any
  stages { 
        stage('Deploy') {
          steps {
              sh "cd .."
              sh 'ls -al'
              // sh 'mkdir -p frontend'
              // script{
              //   zip zipFile: 'frontend.zip', archive: false, dir: './'
              // }
              // sh 'ls -al'
            }
          }
        }
  }
  //   post {
  //     always {
  //         archiveArtifacts artifacts: 'frontend.zip', fingerprint: true
  //     }
  // }
