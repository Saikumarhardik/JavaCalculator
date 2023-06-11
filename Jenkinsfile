pipeline{
    agent{
        label "qwertyy"
    }
        stages{
            stage ('building sonar'){
                steps {
                    withSonarQubeEnv('sonarqube_java_calculator'){
                        sh "mvn sonar:sonar"
                    }
                    
                }
            }
        }
}
                
         
