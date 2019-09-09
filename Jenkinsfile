pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
			post {
				success {
					echo 'New Archiving...'
					archiveArtifacts artifacts: '**/*.war'
				}
			}
        }
    }
}