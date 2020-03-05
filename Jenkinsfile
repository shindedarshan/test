node('docker') {
 
    stage 'Checkout'
        checkout scm
		
    stage 'Build image'
        sh "docker build -t user-management:latest -f docker-compose.yml ."
        
  
    stage 'Push image'
		sh "docker login -u thertion12 -p *Batu_20110656*"
		sh "docker push thertion12/user_management"
}
