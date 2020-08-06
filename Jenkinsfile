
pipeline {
    agent any
    stages {
        stage('One') {
            steps {
                echo 'Step 1..'
            }
        }
		stage('Two') {
            steps {
                input('Want to proceed?')
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
						agent {
							docker {
								reuseNode false
								image 'ubuntu'
							}
						}
					}
					steps {
						echo 'running integration test'
					}
				}
			}
		}
	}
}