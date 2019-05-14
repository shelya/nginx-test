pipeline {
  agent any
  stages {
    stage('get source') {
      steps {
        git(url: 'https://github.com/shelya/nginx-test.git', branch: 'master')
      }
    }
    stage('Run ansible') {
      steps {
        ansiblePlaybook(playbook: 'ansible/nginx.yml', credentialsId: 'root_nginx', disableHostKeyChecking: true, inventory: 'ansible/hosts', limit: 'nginx-hosts')
      }
    }
  }
}