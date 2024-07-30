//Declarative
pipeline {
	agent any 
	//agent { docker { image 'alpine:3.19'}}
	environment{
		dockerHome =tool 'myDocker'
		mavenHome =tool 'myMaven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}
 stages{
		stage('Build'){
           steps{
			sh 'mvn --verison'
			sh 'docker verison'
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
			echo 'I am aweasome,I run always'
		}
		success{
			echo 'I run when you are succesful'
		}
		failure{
			echo 'I run when you fail'
		}
	}

}
