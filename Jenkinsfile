pipeline {

	agent any

	stages {
	    stage('Checkout') {
	        steps {
			checkout scm			       
		      }}
		stage('Build') {
	           steps {
			   sh '/home/diksha/Documents/D1/apache-maven-3.6.3/bin/mvn install'
	                 }}
		stage('Deployment'){
		    steps {
			   sh 'sshpass -p "dev" scp target/LoginWebApp.war dev@172.17.0.3:/home/dev/demo/apache-tomcat-8.5.64/webapps'
			}}
       		
	}
}
