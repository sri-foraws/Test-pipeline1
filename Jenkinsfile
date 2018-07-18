
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building.. step'
				sh 'make'
				
            }
        }
		stage('script'){
			steps{
					script{
					writeFile file: 'output.txt', text: 'asdf testing message'
					env.FILENAME = readFile  'output.txt'
					}
			}
		}
        stage('Test') {
            steps {
                echo 'Testing..'
				echo "${env.FILENAME}"
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