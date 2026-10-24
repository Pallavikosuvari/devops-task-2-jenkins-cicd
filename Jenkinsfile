pipeline {
    agent any

    environment {
        IMAGE_NAME     = 'devops-task-2-app'
        CONTAINER_NAME = 'devops-task-2-container'
        APP_PORT       = '3000'
        HOST_PORT      = '3000'
    }

    triggers {
        pollSCM('H/2 * * * *')
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm ci'
            }
        }

        stage('Test') {
            steps {
                sh 'npm test'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t $IMAGE_NAME:$BUILD_NUMBER -t $IMAGE_NAME:latest .'
            }
        }

        stage('Deploy') {
            steps {
                sh '''
                    docker stop $CONTAINER_NAME || true
                    docker rm $CONTAINER_NAME || true
                    docker run -d --name $CONTAINER_NAME -p $HOST_PORT:$APP_PORT $IMAGE_NAME:latest
                '''
            }
        }
    }

    post {
        success {
            echo 'Pipeline succeeded: app built and deployed!'
        }
        failure {
            echo 'Pipeline failed. Check the console output.'
        }
    }
}
