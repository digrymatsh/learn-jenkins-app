pipeline {
    agent any

    stages {
        stage('Build') {
            docker {
                image 'node:18'
            }
            
            steps {
                sh '''
                ls -la
                node --version
                npm --version
                npm ci
                npm run build
                '''
            }
        }
    }
}