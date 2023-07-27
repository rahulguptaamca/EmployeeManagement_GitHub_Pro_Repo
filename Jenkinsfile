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
	  try{
	  	withCredentials([<object of type com.cloudbees.jenkins.plugins.awscredentials.AmazonWebServicesCredentialsBinding>]) {
         sh "aws s3 ls"
       }
	  }
	 }
	}
}