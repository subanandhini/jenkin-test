pipeline {
  agent any
	tools {
		jdk "JDK_HOME"
		maven "maveen"
	}
  stages {
	  stage('Test'){
		  steps{
			  bat 'java -version'
			  bat 'mvn -version'
			  bat 'echo Testing Completed Successfully'
		  }
          
	  }
      stage('Build'){
		  steps{
			  bat 'mvn claen install'
		  }
          
	  }
      stage('Deploy'){
		  steps{
			  deploy adapters: [tomcat8(credentialsId: 'admin', path: '', url: 'http://localhost:9000/')], contextPath: null, war: 'target/Jenkins.war'
		  }
          
	  }
  }
}
