pipeline {
    agent any
    stages {
        stage('start the selenium grid') {
            steps {
                //sh
                bat "docker-compose up -d hub chrome firefox"
            }
        }
		stage('run the tests') {
            steps {
                //sh
                bat "docker-compose up search-module1 search-module2 flight-module1 flight-module2"
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