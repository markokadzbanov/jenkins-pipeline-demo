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
                sh 'echo "docker build -t demo-image ."'
            }
        }

        stage('Push image') {
            steps {
                sh 'echo "docker push demo-image"'
            }
        }
    }
}
