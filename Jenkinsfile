pipeline {
	agent any 
	triggers {
  pollSCM '* * * * *'
}

	parameters {
		choice(name: 'ENVIRONMENT', choices: ['QA','UAT'], description: 'Pick Environment value')
	}

  choice choices: ['DEV', 'UAT', 'QA', 'PROD'], description: 'parameterized', name: 'Environment'
}
 (pipeline)
	stages {
	    stage('Checkout') {
	        steps {
			checkout scm			       
		      }}
		stage('Build') {
	           steps {
			  sh '/home/shantanu/Downloads/apache-maven-3.9.5-bin/apache-maven-3.9.5/bin/mvn install'
	                 }}
		stage('Deployment'){
		   steps {
		sh 'cp target/oneplus.war /home/shantanu/Downloads/apache-tomcat-9.0.82/webapps
'
			}}	
}}
