pipeline {
  agent any
  stages {
    stage('checkout stage') {
      steps {
        sh 'rm -rf Ansible_project'
        sh 'git clone https://github.com/yatheesh2328/Ansible_project.git'
      }
    }
    stage('checking connection') {
      steps {
        sh 'ansible all -m ping'
      }
    }
    stage('running playbook') {
      steps {
        sh 'ansible-playbook -i hosts sample.yml'
      }
    }
  }
}
