pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                sh 'java -version'
                sh 'mvn -version'
                sh 'mvn clean package'
            }
        }
    }

    post {
        success {
            echo 'Build success'
        }
        failure {
            echo 'Build failed, check console output'
        }
    }
}

