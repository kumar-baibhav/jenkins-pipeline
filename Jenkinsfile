
pipeline {
    agent any
    stages {
        stage('One') {
            agent { docker 'openjdk:8-jre' } 
            steps {
                echo 'Hello, JDK'
                sh 'java -version'
            }
        }
		stage('Two') {
            steps {
                sh 'java -jar exp-0.0.1-SNAPSHOT-jar-with-dependencies.jar'
            }
        }
		stage('Three') {
            parallel {
                stage('Unit Test') {
					steps {
						echo 'running unit test'
					}
				}
				stage('Integration test') {
					steps {
						echo 'running integration test'
					}
				}
			}
		}
	}
}