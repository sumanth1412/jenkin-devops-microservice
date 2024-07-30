//Declarative
pipeline {
	//agent any 
	agent { docker { image 'alpine:3.19'}}
 stages{
		stage('Build'){
           steps{
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
