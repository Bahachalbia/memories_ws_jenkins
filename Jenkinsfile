pipeline {
    agent any
    
    environment {
        DOCKERHUB_CREDENTIALS = credentials('docker_jinkins')
        }
    stages {
     
        stage('build') {
            steps {
                sh 'sudo docker compose up -d' 
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
