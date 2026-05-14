pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Install Streamlit') {
            steps {
                sh 'python -m pip install streamlit'
            }
        }

        stage('Run App') {
            steps {
                sh 'python -m streamlit run streamlit_app.py --server.port 8501 &'
            }
        }
    }

    post {
        success {
            echo "SUCCESS 🚀 Streamlit is running"
        }
    }
}