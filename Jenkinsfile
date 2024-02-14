pipeline {
    agent any

    environment {
        // Correct credential ID for Docker Hub credentials
        DOCKERHUB_CREDENTIALS = credentials('5e2c6607-bcbf-4e48-9079-f0b2e6f415ce')
        DOCKER_IMAGE = 'your-dockerhub-username/your-image-name'
    }

    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    docker.build("${DOCKER_IMAGE}:${BUILD_NUMBER}")
                }
            }
        }
    }
}
