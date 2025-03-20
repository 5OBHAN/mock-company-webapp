pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh './gradlew assemble'
            }
        }

        stage('Test') {
            steps {
                sh './gradlew test'
            }
        }
    }

    post {
        success {
            echo 'Continuous Integration: SUCCESSFUL!'
        }
        failure {
            echo 'Continuous Integration: FAILED!'
        }
    }
}
