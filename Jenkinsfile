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
        dockerfile {
              args '-u root:sudo -v /usr/share/jenkins'
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
  }
}