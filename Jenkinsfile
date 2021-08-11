node {
	def app
	stage ('Clone repository') {
		/* Cloning the repository to our worksapce */
		checkout scm
	}

	stage('Build image') {
		/* this build the image */
		app = docker.build("evaligm/psspimg4")
	}

	}

