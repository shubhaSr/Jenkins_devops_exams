pipeline {
    agent any

    environment {
        DOCKERHUB_CREDENTIALS = credentials('jenkins-dockerhub')
    }

    stages {
        stage("Git Clone") {
            steps {
                git branch: 'main', credentialsId: 'Jenkins', url: 'https://github.com/shubhaSr/Jenkins_devops_exams.git'
            }           
        } 

        stage('Build') {
            steps {
                sh "docker build -t aftab70/custom_apache:${BUILD_NUMBER} ./cast-service/"
            }
        }

        stage('Login') {
            steps {
                sh "echo \$DOCKERHUB_CREDENTIALS_PSW | docker login -u \$DOCKERHUB_CREDENTIALS_USR --password-stdin"
            }
        }

        stage('Push') {
            steps {
                sh "docker push aftab70/custom_apache:${BUILD_NUMBER}"
            }
        }
    }


}
