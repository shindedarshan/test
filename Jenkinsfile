node {
 
    stage 'Checkout'
        checkout scm
		
    stage 'Build image'
        sh label: '', script: '''docker-compose build
				 docker-compose up'''
        
  
    stage 'Push image'
		sh "docker login -u thertion12 -p *Batu_20110656*"
		sh "docker push thertion12/user_management"
}
