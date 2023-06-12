pipeline{
    agent{
        label "qwertyy"
    }
    stages{
        stage ("building docker"){
            steps{
                sh "docker image  build -t  httpd:2 ."
                
            }
        }
        stage ("creating the container"){
            steps{
                sh "docker container run -dt --name newcont  httpd:2"
            }
        }
        stage ("testing with sonarqube"){
            steps{
                withSonarQubeEnv("sonarsonar"){
                sh "mvn sonar: sonar"
                }
            }
        }
    }
   
}
     
