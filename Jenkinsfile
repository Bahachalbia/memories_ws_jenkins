pipeline {
    agent any
    
    stages {
        stage('build') {
            steps {
                bat 'cd client && npm install' 
            }
        }

        stage('testing') {
            steps {
                echo "testing...."
            }
        }
    }
}
