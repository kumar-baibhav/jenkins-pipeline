
pipeline {
    agent any
    stages {
		stage('One') {
            steps {
                START_PROCESS_INSTANCE = bat (
									script: 'curl -d "{}" -H "Content-Type: application/json"   http://localhost:8091/engine-rest/process-definition/key/bpmn-process/start',
									returnStatus: true
								) == 0
				echo "Process instance creation : ${START_PROCESS_INSTANCE}"
				//bat 'curl -d "{}" -H "Content-Type: application/json"   http://localhost:8091/engine-rest/process-definition/key/bpmn-process/start'
            }
        }
		stage('Two') {
			when {
				${START_PROCESS_INSTANCE} true
			}
            steps {
				//if (${START_PROCESS_INSTANCE})
                bat '"C:/Program Files/Zulu/zulu-8/bin/java" -jar C:/Users/kumar/Desktop/Tasks/abot-bpmn/ABotBPMN-Client/target/ABotBPMN-Client-0.0.1-SNAPSHOT-jar-with-dependencies.jar'
            }
        }
		
	}
}