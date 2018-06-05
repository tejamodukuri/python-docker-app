node{
   
   stage("App Build started"){
      echo 'App build started..'
git credentialsId: 'fe839c8e-3f44-4a7e-b8c4-97f8ac3fc0e7', url: 'https://github.com/tejamodukuri/python-docker-app'
      }
   
   stage('Docker Build') {
     def app = docker.build "tejamodukuri/pythondocker"
    }
   
   stage("Tag & Push image"){
withDockerRegistry(credentialsId: '085f3b9e-6cb0-4961-9aae-391eba385e8a', url: 'https://github.com/tejamodukuri/python-docker-app.git') {
          sh 'docker tag docker.io/tejamodukuri/pythondocker docker.io/tejamodukuri/pythondocker:001'
          sh 'docker push docker.io/tejamodukuri/pythondocker'
          sh 'docker push docker.io/tejamodukuri/pythondocker:001'

              }
    }
   
    stage('App deployed to Docker') {
     echo 'App deployed to Hub..'
    }

   
























}
