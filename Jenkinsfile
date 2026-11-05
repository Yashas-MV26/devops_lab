pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Run Application') {
            steps {
                sh 'python3 app.py'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'python3 test.py'
            }
        }

        stage('Build') {
            steps {
                echo 'Build completed successfully'
            }
        }
    }

    post {
        success {
            echo 'Jenkins Build Successful'
        }

        failure {
            echo 'Jenkins Build Failed'
        }
    }
}
