// node {
//    def app
//    stage('Build Docker Image') {
//        checkout scm
//        app = docker.build("gramae/docker-react -f Dockerfile.dev .")
//    }

//    stage('Docker Run') {
//        checkout scm
//        app = docker.run("gramae/docker-react npm run test -- --coverage")
//    }
// }

pipeline {
    agent {
         dockerfile //true  
        {
               args '-u root:sudo -v /var/lib/jenkins/workspace/pipeline_react'
           }
    }
    stages{
        
        stage ('Build the image') {
          steps {
             echo 'Starting to build the image'
             script{
                 def jenkinsImage = docker.build("gramae/docker-react -f Dockerfile.dev .")
             }
        }
        
    }
      stage ('Run the image') {
          steps {
             echo 'Runining the image'
             script{
                 def jenkinsImage = docker.run("gramae/docker-react -f Dockerfile.dev .")
             }
        }
        
    }
  }
}