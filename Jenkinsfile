pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat 'mvn.cmd clean package'
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