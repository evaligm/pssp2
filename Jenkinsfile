node {
	def app
	stage ('Clone repository') {
		/* Cloning the repository to our worksapce */
		checkout scm
	}

	stage('Build image') {
		/* this build the image */
		app = docker.build("evaligm/psspimg5")
	}

	stage('Test image') {
		app.inside { echo "tests passed" }
	}


	stage('Push image')  { 
    		docker.withRegistry('https://registry.hub.docker.com', 'Dochub') {
        		app.push("${env.BUILD_NUMBER}")
		app.push("latest")
		}	
		 /* Push the container to the custom Registry */
        		echo "push docker build to dockerhub"
		
		/* clean workspace */
		cleanWs()
               }
}
