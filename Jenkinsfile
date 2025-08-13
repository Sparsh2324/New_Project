pipeline {
    agent any

    stages {
        stage('Verify the configuration') {
            steps {
                echo 'Building..'
                sh '''
                docker info
                docker version
                docker compose version
                '''
            }
        }
        stage('remove docker data') {
            steps {
                echo 'Deploying..'
                sh 'docker system prune -a --volumes -f'
            }
        }
        stage(clonning the repository){
            steps {
                git branch: 'main', url: 'https://github.com/Sparsh2324/New_Project.git'
            }
        }
        stage('Start the container') {
            steps {
                echo 'start the container....'
                sh 'docker compose up -d'
                sh 'docker compose ps'
            }
        }
    }
}