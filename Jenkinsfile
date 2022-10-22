pipeline {
    agent any

    stages {
        stage('build') {
            steps {
                sh 'cd'
                sh 'cd /home/zied/ws-docker-memo'
                sh 'docker commpose up -d'
            
            }
        }

        stage('testing') {
            steps {
                echo "testing...."
            }
        }
    }
}
