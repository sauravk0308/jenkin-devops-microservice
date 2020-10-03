pipeline {
	agent any
	stages {
		stage('Build'){
			steps{
				echo "Build"
			}
		}
		stage('Test'){
			steps{
				echo "Build"
			}
		}
		stage('Integration Test'){
			steps{
				echo "Build"
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
