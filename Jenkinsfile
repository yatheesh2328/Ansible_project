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
        ansiblePlaybook credentialsId: '4baafd19-7e7a-43bc-b5ac-dabce8427b15', disableHostKeyChecking: true, installation: 'Ansible', inventory: '/etc/ansible/hosts', playbook: '/etc/ansible/sample.yml', vaultTmpPath: ''
      }
    }
  }
}
