node {
   deff app
   stage('Build Docker Image') {
       checkout scm
       app = docker.build("gramae/docker-react -f Dockerfile.dev .")
   }

//    stage('Docker Run') {
//        checkout scm
//        app2 = docker.run("gramae/docker-react npm run test -- --coverage")
//    }
}