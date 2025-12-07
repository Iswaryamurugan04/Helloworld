pipeline {
    agent any

    environment {
        DOCKER_IMAGE = "jenkins-docker-demo:latest"
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'feature/jenkins-docker-demo', url: 'https://github.com/Iswaryamurugan04/Helloworld.git'
            }
        }

        stage('Cleanup Old Container') {
            steps {
                // stop & remove old container if exists
                bat "docker stop demo_container || exit 0"
                bat "docker rm demo_container || exit 0"
            }
        }

        stage('Build Docker Image') {
            steps {
                // force rebuild without cache
                bat "docker build --no-cache -t %DOCKER_IMAGE% ."
            }
        }

        stage('Run New Container') {
            steps {
                // run fresh container with latest code
                bat "docker run -d -p 3000:3000 --name demo_container %DOCKER_IMAGE%"
            }
        }
    }
}
