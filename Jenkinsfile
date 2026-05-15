pipeline {
    agent any

    stages {

        stage('Checkout SCM') {
            steps {
                echo 'Cloning Repository...'
                checkout scm
            }
        }

        stage('Checkout') {
            steps {
                echo 'Checking files...'
                sh 'ls -la'
            }
        }

        stage('Install') {
            steps {
                echo 'Installing dependencies...'
                sh 'python3 --version || true'
                sh 'pip --version || true'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                sh 'echo "Application deployed successfully 🚀"'
            }
        }
    }

    post {
        success {
            echo 'Pipeline SUCCESS ✅'
        }

        failure {
            echo 'Pipeline FAILED ❌'
        }
    }
}