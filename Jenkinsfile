node {
     stage 'Checkout'
        checkout scm
		
     stage 'Build image'
        bat "docker-compose -f docker-compose.yml build"
        
     stage 'Test image'
     	bat "docker-compose -f docker-compose.yml up"
     
     stage 'Push image'
	bat "docker push thertion12/user_management"
}
