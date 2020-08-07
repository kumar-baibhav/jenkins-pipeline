
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
                bat '"C:/Program Files/Zulu/zulu-8/bin/java" -jar C:/Users/kumar/eclipse-workspace/exp/target/exp-0.0.1-SNAPSHOT-jar-with-dependencies.jar'
            }
        }
	}
}