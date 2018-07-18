
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building.. step'
				sh 'make'
				def userName = 'Jenkins'
				echo 'Hello Mr. ${userName}'
				echo "I said Hello Mr. ${userName}"
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