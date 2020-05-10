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
                bat "docker-compose up search-module flight-module"
            }
        }
    }
	post{
	    always{
		    archiveArtifacts artifacts: 'output/**'
		    bat "docker-compose down"
		}
	}
}