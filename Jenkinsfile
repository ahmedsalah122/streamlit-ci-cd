pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Check Environment') {
            steps {
                sh 'echo "Checking Jenkins environment..."'
                sh 'python3 --version || echo "Python not installed in Jenkins"'
                sh 'pip --version || echo "pip not available"'
            }
        }

        stage('List Project Files') {
            steps {
                sh 'ls -la'
            }
        }
    }

    post {
        success {
            echo "CI SUCCESS 🚀 Jenkins is working"
        }
        failure {
            echo "CI FAILED ❌"
        }
    }
}