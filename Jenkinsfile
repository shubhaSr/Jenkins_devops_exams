pipeline {
    agent any

    environment {
        // Correct credential ID for Docker Hub credentials
        DOCKERHUB_CREDENTIALS = credentials('5e2c6607-bcbf-4e48-9079-f0b2e6f415ce')
    }

    stages {
        stage("Git Clone") {
            steps {
                git branch: 'main', credentialsId: '93689f95-a7e8-4d7f-8693-581bc1959b7a', url: 'https://github.com/shubhaSr/Jenkins_devops_exams.git'
            }           
        } 
    }
}
