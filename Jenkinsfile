pipeline {
  agent any
  stages { 
        stage('Deploy') {
          steps {
                sshagent (credentials: ['100-monosparta-loadbalancer']) {
                sh "ssh -T deploy@10.2.9.100"
                sh "ls -al"
              }
            }
          }
        }    
  }
