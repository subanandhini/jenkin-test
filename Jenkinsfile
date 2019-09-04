pipeline {
  agent any
	tools {
		jdk "JDK_HOME"
		maven "maveen"
	}
  stages {
	  stage('Test'){
		  steps{
			  sudo 'java -version'
			  sudo 'mvn -version'
			  sudo 'echo Testing Completed Successfully'
		  }
          
	  }
      stage('Build'){
		  steps{
			  sudo 'mvn clean install'
		  }
          
	  }
      stage('Deploy'){
		  steps{
			  deploy adapters: [tomcat8(credentialsId: 'admin', path: '', url: 'http://localhost:9000/')], contextPath: null, war: 'target/JenkinsOne.war'
		  }
          
	  }
  }
}
