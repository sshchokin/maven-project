pipeline {
    agent any
    tools {
        maven 'localMaven'
    }	
    stages {
        stage('Build') {
            steps {
                bat 'mvn package'
            }
			post {
				success {
					echo 'New Archiving...'
					archiveArtifacts artifacts: '**/target/*.war'
				}
			}
        }
    }
}