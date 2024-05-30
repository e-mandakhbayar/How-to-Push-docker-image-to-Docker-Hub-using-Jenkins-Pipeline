pipeline{

	agent {
    		docker { image 'node:20-alpine' }
  	}

	stages {
	    
	    stage('gitclone') {

			steps {
				git 'https://github.com/e-mandakhbayar/How-to-Push-docker-image-to-Docker-Hub-using-Jenkins-Pipeline'
			}
		}

		stage('Build') {

			steps {
				sh 'docker build -t thetips4you/nodeapp_test:latest .'
			}
		}
	}
}
