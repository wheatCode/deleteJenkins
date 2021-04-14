pipeline {
  agent any
  stages { 
        stage('Deploy') {
          steps {
              sh 'ls -al'
            sshagent (credentials: ['10.2.9.100']) {
              sh "ssh -vvv -o StrictHostKeyChecking=no -T root@10.2.9.100"
              sh "ls -al"
            }
          }
        }
  }
}
