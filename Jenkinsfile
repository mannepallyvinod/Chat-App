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
        stage('Run') {
            steps {
                script {
                    dockerContainer = dockerImage.run("-p 8080:3700 /bin/bash")
                    dockerContainerId = dockerContainer.id
                }
            }
        }
    }
}
