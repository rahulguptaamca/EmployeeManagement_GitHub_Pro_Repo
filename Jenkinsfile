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
	  	withCredentials([[$class: 'AmazonWebServicesCredentialsBinding', accessKeyVariable: 'AWS_ACCESS_KEY_ID', credentialsId: 'deploytos3', secretKeyVariable: 'AWS_SECRET_ACCESS_KEY']]) {
         sh "aws s3 ls"
        }
	  }
	 }
	}
}