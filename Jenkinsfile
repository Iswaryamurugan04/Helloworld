pipeline {
    agent {
        docker {
            image 'node:18'
            args '-w /home/jenkins_project' // sets working directory inside container
        }
    }
    stages {
        stage('Install') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                sh 'npm test'
            }
        }
    }
}
