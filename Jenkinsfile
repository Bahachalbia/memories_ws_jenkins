pipeline {
    agent any
    
    stages {
        stage('build') {
            steps {
                sh 'cd client && npm install' 
            }
        }

        stage('testing') {
            steps {
                echo "testing...."
            }
        }
    }
}
