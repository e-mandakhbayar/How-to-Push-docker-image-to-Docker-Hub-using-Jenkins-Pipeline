pipeline{

	agent any

	

	stages {
	    
	    stage('gitclone') {

			steps {
				git 'https://github.com/shazforiot/nodeapp_test'
			}
		}
	     	stage('Initialize'){
        		def dockerHome = tool 'myDocker'
        		env.PATH = "${dockerHome}/bin:${env.PATH}"
   		 }

		stage('Build') {

			steps {
				sh 'docker build -t thetips4you/nodeapp_test:latest .'
			}
		}
	}
}
