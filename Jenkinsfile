pipeline {
  agent any
  stages { 
        stage('Deploy') {
          steps {
              sh 'ls -al'
              zip zipFile: 'frontend.zip', archive: false, dir: './'
              sh 'ls -al'
            }
          }
        }
  }
}
