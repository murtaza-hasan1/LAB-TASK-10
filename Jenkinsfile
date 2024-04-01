pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/murtaza-hasan1/LAB-TASK-10'
            }
        }

        stage('Dependency Installation') {
            steps {
                bat 'npm install'
            }
        }

        stage('Build') {
            steps {
                bat 'npm run build'
            }
        }

        stage('Test') {
            steps {
                bat 'npm test'
            }
        }

        stage('Containerized') {
            steps {
                bat 'echo containerization'
            }
        }
    }

    post {
        always {
            bat 'docker-compose down'
        }
    }
}
