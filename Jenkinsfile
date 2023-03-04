pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                git url: "https://github.com/mannepallyvinod/Chat-App.git"
            }
        }
        stage('Build') {
            steps {
                script {
                    dockerImage = docker.build("chat-app")
                }
            }
        }
    }
}
