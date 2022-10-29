pipeline {
    agent any
    tools {
        nodejs '19.0.0'
         }
    stages {
        stage('build') {
            steps {
                sh 'cd client ' 
            }
        }
        stage('run') {
            steps {
                sh 'npm install ' 
            }
        }

        stage('testing') {
            steps {
                echo "testing...."
            }
        }
    }
}
