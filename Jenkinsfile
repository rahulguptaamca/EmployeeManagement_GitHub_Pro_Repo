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
         withCredentials([[$class: 'AmazonWebServicesCredentialsBinding', accessKeyVariable: 'AWS_ACCESS_KEY_ID', credentialsId: 'deploytos3', secretKeyVariable: 'AWS_SECRET_ACCESS_KEY']]) {
           sh "/usr/local/bin/aws s3 cp Main.java s3://myfirststhree"
        }
	  }
	 }
	}
}