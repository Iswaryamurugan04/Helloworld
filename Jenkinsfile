pipeline {
    agent {
        docker {
            image 'node:18'
            args '-v /tmp:/tmp -w /tmp'
        }
    }
    stages {
        stage('Echo') {
            steps {
                sh 'echo "Docker is working!"'
            }
        }
    }
}
