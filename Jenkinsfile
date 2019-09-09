pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
			    unstash 'app'
                bat 'mvn clean package'
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