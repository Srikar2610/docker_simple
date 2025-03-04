pipeline {
    agent any

    environment {
        DOCKER_IMAGE = 'srikar2610/my-app:latest'
    }

    stages {
        stage('Clone Repository') {
            steps {
                git url:'https://github.com/srikar2610/docker_simple.git',branch: 'main'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t $DOCKER_IMAGE .'
            }
        }
        stage('Push Docker Image') {

            steps {

                withDockerRegistry([credentialsId: 'docker-hub-credentials', url: 'https://index.docker.io/v1/']) {

                    sh 'docker push $DOCKER_IMAGE'

                }

            }

        }

    }

<<<<<<< HEAD

}

=======

}

>>>>>>> 10d5eb4d4342399871153cea4076266d61c4864d


