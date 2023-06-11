pipeline{
    agent{
        label "qwertyy"
    }
    stages{
        stage ("building docker"){
            steps{
                sh "docker image  build -t  httpd:1 ."
                
            }
        }
        stage ("creating the container"){
            steps{
                sh "docker container run -dt --name httpdcont httpd:1"
    }
   
}
     
