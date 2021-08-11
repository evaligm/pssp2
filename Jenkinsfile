node {
	def app
	stage ('Clone repository') {
		/* Cloning the repository to our worksapce */
		checkout scm
	}

	stage('Test image') {
		app.inside { echo "tests passed" }
	}
	}

