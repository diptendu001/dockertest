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
            sh "docker build --tag=pysample-v2 ."
            sh "docker tag pysample-v2 diptendu001/test100:pysample-14092020"
           }
          }
         }
       stage('Deploye image to Docker')
          {
          steps
           {
           script
             {
             sh "docker push diptendu001/test100:pysample-14092020"
             }
           }
          }
     }
  }


