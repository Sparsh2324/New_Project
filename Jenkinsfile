pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh '''
                docker info
                docker version
                docker compose version
                '''
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying..'
            }
        }
        stage('Push to dockerhub') {
            steps {
                echo 'push to dockerhub....'
            }
        }
    }
}