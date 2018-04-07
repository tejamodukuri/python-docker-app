node{
   
   stage("App Build started"){
      echo 'App build started..'
git credentialsId: '9c5600a6-c0d3-4e81-a2b3-cca6d7257abb', url: 'https://github.com/pavants52/python-docker-app.git'
      }
   
   stage('Docker Build') {
     def app = docker.build "pavan52/pythondocker"
    }
   
   stage("Tag & Push image"){
withDockerRegistry([credentialsId: 'Docker-ID', url: 'https://hub.docker.com/']) {
          sh 'docker tag pavan52/pythondocker pavan52/pythondocker:001'
          sh 'docker push pavan52/projects'
              }
    }
   
    stage('App deployed to Docker') {
     echo 'App deployed to Hub..'
    }

   
























}
