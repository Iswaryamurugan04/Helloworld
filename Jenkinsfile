pipeline {
    agent any
    stages {
        stage('Run Docker') {
            steps {
                bat 'docker pull ubuntu:latest'
                bat 'docker run ubuntu:latest echo Hello from container'
            }
        }
    }
}
