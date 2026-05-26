pipeline {
    agent any
    environment {
        COMPOSE_PROJECT_NAME = "chesstient_${BUILD_NUMBER}"
    }
    stages {
        stage("Checkout") {
            steps {
                checkout scm
            }
        }
        stage("Build Docker") {
            steps {
                sh "docker compose up -d"
            }
        }
    }
}
