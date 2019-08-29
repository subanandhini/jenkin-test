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
  	/*stage('Build') {
	  steps {
	  sh 'mvn clean package'
	 // archiveArtifacts 'target/Jenkins.war'
	  }
  	}
	  stage('Deploy'){
		  steps {
			  deploy adapters: [tomcat8(credentialsId: 'admin', path: '', url: 'http://localhost:8010')], contextPath: null, war: 'target/Jenkins.war'
		  }
	  }*/
  }
}
