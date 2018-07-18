
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
		
			environment{
			
				my_var = "${env.BUILD_ID + '/working'}"
			}
		
			steps{
					script{
					writeFile file: 'output.txt', text: 'asdf testing message'
					env.FILENAME = readFile  'output.txt'
					}
					sh 'mkdir -p $my_var'
					sh 'touch $my_var/test.txt'
					sh 'export MY_EX = $my_var/test.txt'
					
					sh 'echo $MY_EX'
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