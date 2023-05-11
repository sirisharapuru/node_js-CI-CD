pipeline {
environment {
AWS_ACCOUNT_ID="765127052235"
AWS_DEFAULT_REGION="ap-south-1"
IMAGE_REPO_NAME="nodejs-cicd"
IMAGE_TAG="${BUILD_NUMBER}"
REPOSITORY_URI = "${AWS_ACCOUNT_ID}.dkr.ecr.${AWS_DEFAULT_REGION}.amazonaws.com/${IMAGE_REPO_NAME}"
}
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
     
