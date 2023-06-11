pipeline{
    agent{
        label "qwertyy"
    }
    stages{
        stage ("building docker"){
            steps{
                sh "docker image  build -t  java:1 ."
            }
        }
    }
}
     
