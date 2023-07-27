pipeline {
	agent any

	stages{
	 stage('build with version'){
	   steps {

	     sh "java --version"
	     sh "ls"
	   }
	 }

	 stage('deploy'){
	  steps{
	   sh "aws s3 cp demo.html s3://myfirststhree"
	  }
	 }
	}
}