pipeline {
    agent {
        docker {
            image 'node:18'
            args '-v /tmp:/tmp' // or skip mounting entirely
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
