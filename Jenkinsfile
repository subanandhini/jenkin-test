pipeline {
  agent any
	tools {
		jdk "JDK_HOME"
		maven "maveen"
	}
  stages {
	  stage('Test'){
		  steps{
			  sh 'java -version'
			  sh 'mvn -version'
			  sh 'echo Testing Completed Successfully !!!!!!..... By SanjaySaravanan'
		  }
	  }
  }
}
