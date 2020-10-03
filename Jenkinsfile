pipeline {
	//agent any
	agent {docker {image 'maven:3.6.3'}}
	stages {
		stage('Build'){
			steps {
				sh "mvn --version"
				echo "Build"
			}
		}
		stage('Compile'){
			steps {
				SH "mvn clean compile"
			}
		}

		stage('Test'){
			steps {
				sh "mvn test"
			}
		}
		stage('Integration Test'){
			steps {
				sh "mvn failsafe:integration-test failsafe:verify"
			}
		}
	}
	
	 post {
		always {
			echo 'I am awsome. I run always'
		}
		success {
			echo 'I run when you are successful'
		}
		failure {
			echo 'I run wehn you are failure'
		}
	}
}
