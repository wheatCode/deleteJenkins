pipeline {
  agent any
  stages { 
        stage('Deploy') {
          steps {
                sshagent (credentials: ['100-monosparta-loadbalancer']) {
                sh "ssh  -o StrictHostKeyChecking=no -T deploy@10.2.9.100"
                sh "ssh -v deploy@10.2.9.100"
                sh "sh 'scp frontend.zip udeploy@10.2.9.100:/home/deploy'"
              }
            }
          }
        }    
  }
