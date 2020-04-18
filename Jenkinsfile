pipeline {  environment {
    registry = "diptendu001/test100"
    registryCredential = 'dockerhub'
  }  agent any  stages {
    stage('Building image') {
      steps{
        script {
          sh "systemctl status docker"
        }
      }
    }
