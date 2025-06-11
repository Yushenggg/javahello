pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from the repository
                git 'https://github.com/Yushenggg/javahello.git'
            }
        }
        stage('Build with maven') {
            steps {
                // Run Maven install
                bat 'mvn clean install'
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