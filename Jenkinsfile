pipeline {
  agent any
  stages { 
        stage('Deploy') {
          steps {
              sh 'ls -al'
            sshagent (credentials: ['10.2.9.100']) {
              export SSH_KEY="/path_to_ssh_private_key"
              sh "ssh root@10.2.9.100"
              sh "ls -al"
            }
          }
        }
  }
}
