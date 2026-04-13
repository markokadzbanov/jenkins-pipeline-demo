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
                sh 'docker build -t markokadzbanov/jenkins-demo .'
            }
        }

        stage('Push image') {
            steps {
                sh 'docker login -u markokadzbanov -p dckr_pat_LNWtlOet2MABc7nnCnCW5ZxYHEI'
                sh 'docker push markokadzbanov/jenkins-demo'
            }
        }
    }
}
