//SCRIPTEd


//DECLARATIVE
pipeline {
	agent any
	//agent { docker { image 'maven:3.6.3'}}
	
	//agent { docker { image 'node:13.8'}}
	

	environment {
		dockerHome = tool 'myDocker' 
		mavenHome = tool 'myMaven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}

	 stages{
		stage('Check out') {
			steps{
				    sh 'mvn --version'
			        sh 'docker version'
				
					echo "Build"
					echo "PATH - $PATH"
					echo "BUID_NUMBER - $env.BUID_NUMBER"
					echo "BUID_ID - $env.BUID_ID"
					echo "JOB_NAME - $env.JOB_NAME"
					echo "BUID_TAG - $env.BUID_TAG"
					echo "BUID_URL - $env.BUID_URL"
					}
			
		}
		stage(Compile){

			steps{
				sh "mvn clean compile"
			}
		}

		stage('Test') {
			steps{
				sh "mvn test"
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

