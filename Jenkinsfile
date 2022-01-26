pipeline {
    agent any

    environment {
        CI = 'true'
    }
    
    stages {
        stage('npm install') {
            steps {
                sh 'npm install'
            }
        }

        stage('install client dependencies') {
            steps {
                sh './client'
                sh 'npm install'
            }
        }

        stage('install server dependencies') {
            steps {
                sh '../server'
                sh 'npm install'
            }
            
        }

        stage('build') {
            steps {
                sh 'npm run dev &'
            }
            
        }

        stage('Test'){
            steps {
                sh "curl http://localhost:3006"
            }
        }
    }
}