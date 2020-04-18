pipeline {  
   environment {
    registry = "diptendu001/test100"
    registryCredential = 'dockerhub'
  }  
    agent any  
    stages 
    {
      stage("VERSION")
         {
          steps {
             sh "docker --version"
                }
         }
     
       stage('Building image') 
         {
          steps
           {
           script 
           {
            sh "docker build --tag=pysample-v1 ."
            sh "docker tag pysample-v1 diptendu001/test100:pysample-1804"
           }
          }
         }
       stage('Deploye image to Docker')
          {
          steps
           {
           script
             {
             sh "docker push diptendu001/test100:pysample-1804"
             }
           }
          }
     }
  }


