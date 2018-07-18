
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building.. step'
				sh 'make'
				archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
		stage('Personal') {
			steps{
			   echo 'This is my personal step'
			}
		}
    }
}