pipeline {
  agent any
	tools {
		jdk "JDK_HOME"
		maven "M2_HOME"
	}
  stages {
	  stage('Test'){
		  steps{
			  sh 'java -version'
			  sh 'mvn -version'
			  sh 'echo Testing Completed Successfully'
		  }
          
	  }
      stage('Build'){
		  steps{
			  sh 'mvn clean install'
		  }
          
	  }
      stage('Deploy'){
		  steps{
			  deploy adapters: [tomcat8(credentialsId: 'admin', path: '', url: 'http://localhost:9000/')], contextPath: null, war: 'target/JenkinsOne.war'
		  }
          
	  }
  }
}
