pipeline{
    agent{
        label "abcd"
    }
    stages{
        stage ("packagin the application"){
            steps{
                sh "mvn clean package"
            }
        }
        stage ("testing with sonarqube"){
            steps{
                withSonarQubeEnv("sonarsonar"){
                sh "mvn sonar:sonar"
                }
            }
        }
    }
   
}
     
