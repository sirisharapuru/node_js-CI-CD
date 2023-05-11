pipeline {
  agent any
  stages {
    
    stage('git clone'){
      steps{
        script{
          git branch: 'main', credentialsId: 'git', url: 'https://github.com/syedirfaan6/nodejs-cicd'}}}
         
    stage('build image') {
      steps{
        script {
          dockerImage = docker.build "${IMAGE_REPO_NAME}:${IMAGE_TAG}"
        }
      }
    }
  }
}
     
