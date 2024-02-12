pipeline {
environment { // Declaration of environment variables
DOCKER_ID = "cast" // replace this with your docker-id
DOCKER_IMAGE = "cast-service"
DOCKER_TAG = "v.1.0" // we will tag our images with the current build in order to increment the value by 1 with each new build
}
agent any // Jenkins will be able to select all available agents
stages {
        stage('Docker Build'){ // docker build image stage
            steps {
                script {
                sh '''
                 docker rm -f jenkins
                 cd cast-service
                 docker build -t $DOCKER_ID/$DOCKER_IMAGE:$DOCKER_TAG .
                sleep 6
                '''
                }
            }
        }
