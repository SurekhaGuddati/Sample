pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/SurekhaGuddati/Sample.git', branch: 'main'
            }
        }

        stage('Build') {
            steps {
                // Compile Java program directly
                bat 'javac HelloWorld.java'
            }
        }

        stage('Test') {
            steps {
                // Run the program as a simple test
                bat 'java HelloWorld'
            }
        }

        stage('Deploy') {
            steps {
                // Copy compiled class file to deployment folder
                bat 'copy HelloWorld.class e:\\deployments\\'
            }
        }
    }
}
