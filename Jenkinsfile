pipeline {
    agent any  // Use any available agent

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from the Git repository
                git 'https://github.com/LabharthBagda/TestRepo.git'
            }
        }
        stage('Build') {
            steps {
                // Compile the Java code
                bat 'javac Main.java'  // Compile Main.java
            }
        }
        stage('Run') {
            steps {
                // Run the compiled Java program
                bat 'java Main'  // Run Main class
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed. Check the logs for details.'
        }
    }
}

