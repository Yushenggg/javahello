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
                bat 'mvn package'
            }
        }
    }
    post {

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