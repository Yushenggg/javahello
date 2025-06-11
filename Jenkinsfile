pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from the repository
                git 'https://your-repository-url.git'
            }
        }
        stage('Build') {
            steps {
                // Run Maven install
                sh 'mvn install'
            }
        }
    }
    post {
        always {
            // Archive the build artifacts
            archiveArtifacts artifacts: '**/target/*.jar', allowEmptyArchive: true
        }
        success {
            // Notify success
            echo 'Build succeeded!'
        }
        failure {
            // Notify failure
            echo 'Build failed!'
        }
    }
}