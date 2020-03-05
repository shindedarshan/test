node {
    stage('Code checkout') {
        checkout scm
    }

    stage('Build image') {
		sh "docker-compose build"
    }
	
	stage('Test image') {
		sh "docker-compose up"
	}

    stage('Push image') {
        docker.withRegistry('https://registry.hub.docker.com', 'docker-hub-credentials') {
            sh "docker push thertion12/user_management"
        }
    }
}
