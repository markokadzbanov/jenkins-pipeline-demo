pipeline {
    agent any

    stages {
        stage('Clone repository') {
            steps {
                echo 'Cloning repository...'
            }
        }

        stage('Build image') {
            steps {
                script {
                    docker.build("markokadzbanov/my-nginx-app")
                }
            }
        }

        stage('Push image') {
            steps {
                script {
                    docker.withRegistry('', 'dockerhub-credentials') {
                        docker.image("markokadzbanov/my-nginx-app").push()
                    }
                }
            }
        }
    }
}
