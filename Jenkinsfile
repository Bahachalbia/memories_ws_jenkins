pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'docker compose up -d'
        sh 'cd /home/zied/ws-docker-memo'
        sh 'docker commpose up -d'
      }
    }

  }
}