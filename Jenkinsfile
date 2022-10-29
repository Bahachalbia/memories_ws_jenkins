pipeline {
    agent any
    
    environment {
        DOCKERHUB_CREDENTIALS = credentials('bahachalbia_dockerhub')
        }
    stages {
        stage('build') {
            steps {
                sh 'cd client' 
            }
        }
        stage('build') {
            steps {
                sh 'docker build -t bahachalbia/front:front .' 
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
