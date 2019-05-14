pipeline {
  agent any
  stages {
    stage('get source') {
      steps {
        git(url: 'https://github.com/shelya/nginx-test.git', branch: 'master')
      }
    }
  }
}