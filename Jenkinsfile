pipline {
    agent any

    stages {
      stage ('Build Docker Image') {
        steps {
          script {
            dockerapp = docker.build("cauachagas/kube-news:${env.BUILD_ID}", '-f ./src/Dockerfile ./src')
        }
      }
    }
  }
  
}