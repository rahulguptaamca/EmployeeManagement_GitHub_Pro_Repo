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
           sh "cd ~/.local/bin/ && ./aws s3 ls"
        }
	  }
	 }
	}
}