pipeline {
  agent any
  stages { 
        stage('Deploy') {
          steps {
             sh "echo 1 > build/a.txt"
              sshagent (credentials: ['100-monosparta-loadbalancer']) {
                sh "ssh -o StrictHostKeyChecking=no -T deploy@10.2.9.110"
                sh "ssh ls -al"
                sh "ssh -v deploy@10.2.9.110"
                sh "scp -r build deploy@10.2.9.110:~/"

              }
            }
          }
        }    
  }
