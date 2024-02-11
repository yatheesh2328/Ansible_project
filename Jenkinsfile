pipeline{
  agent {label 'slave1'
         stages{
           stage('checkout stage'){
             steps{
               sh 'git clone https://github.com/yatheesh2328/hello-world-war.git'
               sh. 'ansible-playbook sample.yml'
             }
           }
         }
        }
}
