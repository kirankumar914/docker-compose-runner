pipeline {
    agent any
    stages {
        stage('Run the tests') {
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