pipeline {
  agent any
  stages { 
        stage('Deploy') {
          steps {
             sh "mkdir /build"
              sshagent (credentials: ['100-monosparta-loadbalancer']) {
                sh "ssh -o StrictHostKeyChecking=no -T deploy@10.2.9.110"
                sh "ssh -v deploy@10.2.9.110"
                sh "scp -r /build/* deploy@10.2.9.110:/var/www/gohiking-web"
              }
            }
          }
        }    
  }
