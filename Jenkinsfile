pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from the repository
                git 'https://github.com/Yushenggg/javahello.git'
            }
        }
        stage('Build') {
            steps {
                // Run Maven install
                sh 'mvn -B -DskipTests clean package'
            }
        }
    }
    post {
        always {
            // Archive the build artifacts
            archiveArtifacts artifacts: './target/*.jar', allowEmptyArchive: true
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