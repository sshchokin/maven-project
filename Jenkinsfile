pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
			post {
				echo 'New Archiving...'
				archiveArtifacts artifacts: '**/target/*.war'
			}
        }
    }
}