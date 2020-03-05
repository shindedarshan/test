node {
     stage 'Checkout'
        checkout scm
		
     stage 'Build image'
        sh "docker-compose -f docker-compose.yml build"
        
     stage 'Test image'
     	sh "docker-compose -f docker-compose.yml up"
     
     stage 'Push image'
	sh "docker push thertion12/user_management"
}
