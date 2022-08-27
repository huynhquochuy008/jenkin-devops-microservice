//SCRIPTED

//DECLARATIVE
pipeline {
	// agent any
	agent { docker { image 'maven:3.6.3'} }
	// agent { docker { image 'node:13.8'} }
	eviroments {
		dockerHome = tool 'myDocker'
		mavenHome = tool 'myMaven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}
	stages {
		stage('Checkout') {
			steps {
				sh 'mvn --version' 
				sh 'docker version'
				echo "${STAGE_NAME}"
				echo " BUILD TAG: ${BUILD_TAG}"
			}
		}
		stage('Compile') {
			steps {
				echo "${STAGE_NAME}"

			}
		}

		stage('Test') {
			steps {
				echo "${STAGE_NAME}"
			}
		}

		stage('Integration Test') {
			steps {
				echo "${STAGE_NAME}"
			}
		}

		stage('Package') {
			steps {
				echo "${STAGE_NAME}"
			}
		}

		stage('Build Docker Image') {
			steps {
				echo "${STAGE_NAME}"
			}
		}

		stage('Push Docker Image') {
			steps {
				echo "${STAGE_NAME}"
			}
		}
	} 
	
	post {
		always {
			echo 'Im awesome. I run always'
		}
		success {
			echo 'I run when you are successful'
		}
		failure {
			echo 'I run when you fail'
		}
	}
}
