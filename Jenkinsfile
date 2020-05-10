pipeline {
    agent any
    stages {
        stage('start the selenium grid') {
            steps {
                //sh
                bat "docker-compose up"
            }
        }
        stage('down the infrastructure') {
            steps {
                //sh
                bat "docker-compose down"
            }
        }
    }
}