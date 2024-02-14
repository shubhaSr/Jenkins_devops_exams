pipeline {
    agent any

    environment {
        // Correct credential ID for Docker Hub credentials
        DOCKERHUB_CREDENTIALS = credentials('jenkins-dockerhub')
    }

    stages {
        stage("Git Clone") {
            steps {
                git branch: 'main', credentialsId: 'Jenkins', url: 'https://github.com/shubhaSr/Jenkins_devops_exams.git'
            }           
        } 
    }
}
