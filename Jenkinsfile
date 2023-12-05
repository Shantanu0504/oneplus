pipeline {
	agent any 
	parameters {
<<<<<<< HEAD
		choice(name: 'ENVIRONMENT', choices: ['QA','UAT'], description: 'Pick Environment value')
	}
=======
  choice choices: ['DEV', 'UAT', 'QA', 'PROD'], description: 'parameterized', name: 'Environment'
}
>>>>>>> e3ab802 (pipeline)
	stages {
	    stage('Checkout') {
	        steps {
			checkout scm			       
		      }}
		stage('Build') {
	           steps {
			  sh '/home/guru/slaveDD2/apache-maven-3.9.0/bin/mvn install'
	                 }}
		stage('Deployment'){
		   steps {
		sh 'cp target/flipkart.war /home/swapnil/Documents/DevOps-Software/apache-tomcat-9.0.79/webapps'
			}}	
}}
