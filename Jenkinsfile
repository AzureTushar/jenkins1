//SCRIPTEd


//DECLARATIVE
pipeline{
	agent any

	stages {
		stage('Build') {
			steps{
				echo "Build"
				echo "Test"
				echo "Integration Test"
			}
			
		}
		stage('Test') {
			steps{
				echo "Test"
			}
		}
		stage('Integration Test') {
			steps{
				echo "Integration Test"
			}
		}
		stage('Integration1 Test') {
			steps{
				echo "Integration1 Test"
			}
		}
		stage('Integration2 Test') {
			 steps{
				echo "Integration2 Test"
			 }
		}
	} 
	
	post {
		always {
			echo 'I am Awesome, I always run'
		}
	 
		success{
			echo 'I run when you are successfull'
		}
		failure {
			echo 'I run when you fail'
		}
	}
}

