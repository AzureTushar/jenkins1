//SCRIPTEd


//DECLARATIVE
pipeline {
	//agent any
	agent { docker { image 'maven:3.6.3'}}
	stages {
		stage('Build') {
			steps{
				sh 'mvn --version'
				echo "Build"
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

