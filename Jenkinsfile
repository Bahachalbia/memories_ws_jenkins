pipeline {
    agent any
    
         }
    stages {
        stage('build') {
            steps {
                sh 'cd client ' 
            }
        }
        stage('run') {
            steps {
                sh 'npm version ' 
            }
        }

        stage('testing') {
            steps {
                echo "testing...."
            }
        }
    }
}
