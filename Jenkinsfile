pipeline {
  agent any
  stages { 
        stage('Deploy') {
          steps {
              sh 'ls -al'
            sshagent (credentials: ['10.2.9.100']) {
              sh "ssh -vvv -o StrictHostKeyChecking=no -T deploy@10.2.9.100"
              sh "ls -al"
            }
          }
        }
  }
}
