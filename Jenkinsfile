
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
                bat 'curl -d "{}" -H "Content-Type: application/json"   http://localhost:8091/engine-rest/process-definition/key/bpmn-process/start'
            }
        }
	}
}