pipeline {
    agent any
    
    environment {
        DOCKERHUB_CREDENTIALS = credentials('bahachalbia_dockerhub')
        }
    stages {
        stage('build') {
            steps {
                sh 'docker compose build bahachalbia/front -t front .' 
            }
        }
        stage('login') {
            steps {
                sh 'echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u bahachalbia  ' 
            }
        }

        stage('push') {
            steps {
                sh "docker push bahachalbia/front:front"
            }
        }
    }
}
