pipeline {
    agent any

    stages {

        stage('Checkout Code') {
            steps {
                checkout scm
            }
        }

        stage('Verify Java') {
            steps {
                sh '''
                java -version
                javac -version
                '''
            }
        }

        stage('List Files') {
            steps {
                sh 'ls -la'
            }
        }

        stage('Compile Java') {
            steps {
                sh 'javac HelloWorld.java'
            }
        }

        stage('Run Java Program') {
            steps {
                sh 'java HelloWorld'
            }
        }
    }

    post {
        success {
            echo 'Build executed successfully!'
        }
        failure {
            echo 'Build failed!'
        }
    }
}
