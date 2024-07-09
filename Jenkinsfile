pipeline {
    agent any
    stages {
        stage('Check for running containers') {
            steps {
                script {
                    def mongoRunning = sh(script: 'docker ps -q -f name=mongo', returnStatus: true)
                    def mongoExpressRunning = sh(script: 'docker ps -q -f name=mongoExpress', returnStatus: true)
                    if (mongoRunning == 0 && mongoExpressRunning == 0) {
                        // No running containers found, proceed with docker compose up
                        sh 'docker compose up -d'
                    } else {
                        echo 'mongo or mongoExpress is already running'
                    }
                }
            }
        }
    }
}
