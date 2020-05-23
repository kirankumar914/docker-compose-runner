pipeline {
    agent any
    stages {
	    stage('Pull the latest image') {
            steps {
                //sh
                bat "docker pull kirankumar914/selenium-docker"
            }
        }	
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