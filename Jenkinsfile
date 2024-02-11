pipeline {
  agent {
    label 'slave1'
  }
  stages {
    stage('checkout stage') {
      steps {
        // Remove the directory if it exists
        catchError(buildResult: 'SUCCESS', stageResult: 'FAILURE') {
          sh 'rm -rf Ansible_project'
        }
        // Clone the repository
        catchError(buildResult: 'SUCCESS', stageResult: 'FAILURE') {
          sh 'git clone https://github.com/yatheesh2328/Ansible_project.git'
        }
      }
    }
    stage('running playbook') {
      steps {
        // Run the Ansible playbook
        catchError(buildResult: 'SUCCESS', stageResult: 'FAILURE') {
          sh 'ansible-playbook Ansible_project/sample.yml'
        }
      }
    }
  }
}
