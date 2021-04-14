pipeline {
  agent any
  stages { 
        stage('Deploy') {
          steps {
              sh 'ls -al'
            sshagent (credentials: ['10.2.9.100']) {
              sh "ssh root@10.2.9.100"
              sh "ls -al"
            }
          }
        }
  }
}
