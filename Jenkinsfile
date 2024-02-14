pipeline {
    agent any

    environment {
        // Correct credential ID for Docker Hub credentials
        DOCKERHUB_CREDENTIALS = credentials('5e2c6607-bcbf-4e48-9079-f0b2e6f415ce')
        DOCKER_IMAGE = 'shubha1997/test'
    }

    stages {
         stage("Git Clone") {
            steps {
                git branch: 'main', url: 'https://github.com/shubhaSr/Jenkins_devops_exams.git'
            }           
        }
    }
}
