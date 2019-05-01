node {
   def app
   stage('Build Docker Image') {
       checkout scm
       app = docker.build("gramae/docker-react Dockerfile.dev .")
   }

   stage('Docker Run') {
       checkout scm
       app = docker.run("gramae/docker-react npm run test -- --coverage")
   }
}