pipeline {
  agent any
  stages { 
        stage('Deploy') {
          steps {
              sshagent (credentials: ['100-monosparta-loadbalancer']) {
                sh "ssh -o StrictHostKeyChecking=no -T deploy@10.2.9.110"
                sh "ssh -v deploy@10.2.9.110"
                sh "scp -r * deploy@10.2.9.110:/home/deploy"
              }
            }
          }
        }    
  }
