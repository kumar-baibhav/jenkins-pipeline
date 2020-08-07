
pipeline {
    agent any
    stages {
        stage('One') {
            steps {
                echo 'Hello, JDK'
                bat '"C:/Program Files/Zulu/zulu-8/bin/java" -version'
            }
        }
		stage('Two') {
            steps {
                //java -jar 'exp-0.0.1-SNAPSHOT-jar-with-dependencies.jar'
				echo 'java'
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