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
        stage ("quality gates"){
            steps{
                sh "waitForQualityGate abortPipeline: false, credentialsId: 'sonarid'"
            }
        }
    }
   
}
     
