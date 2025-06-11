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
                
                bat 'set PATH=%PATH%;C:/Applications/Maven/apache-maven-3.9.9/bin'
                bat 'C:/Applications/Maven/apache-maven-3.9.9/bin/mvn clean install'
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