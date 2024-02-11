pipeline {
  agent any
  stages {
    stage('checkout stage') {
      steps {
        sh 'rm -rf Ansible_project'
        sh 'git clone https://github.com/yatheesh2328/Ansible_project.git'
      }
    }
    stage('running playbook') {
      steps {
        ansiblePlaybook credentialsId: 'b82b62d6-07c6-4fa0-8c96-dd3bfa4c09d8', disableHostKeyChecking: true, installation: 'Ansible', inventory: '/etc/ansible/hosts', playbook: '/etc/ansible/sample.yml', vaultTmpPath: ''
      }
    }
  }
}
