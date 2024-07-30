//Declarative
pipeline {
	agent any 
	//agent { docker { image 'alpine:3.19'}}
	environment{
		dockerHome =tool 'myDocker'
		mavenHome =tool 'myMaven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
		DOCKER_HOST = 'unix:///var/run/docker.sock'
	}
 stages{
		stage('Build'){
           steps{
			sh 'mvn --version'
			sh 'docker version'
			echo "Build"
		   }
		}
		stage('Test'){
           steps{
			echo "Build"
			echo "Test"
           }
		}
		stage('Integration Test'){
           steps{
			echo "Integration Test"
		   }
		}
	}
	
	post{
		always{
			echo 'I am awesome,I run always'
		}
		success{
			echo 'I run when you are successful'
		}
		failure{
			echo 'I run when you fail'
		}
	}

}
