pipeline {
    agent {
        docker {
            image 'ubuntu:latest'
        }
    }
    stages {
        stage('Install Git') {
            steps {
                sh 'apt-get update && apt-get install -y git'
                sh 'git --version'
            }
        }
    }
}

