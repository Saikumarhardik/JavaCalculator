pipeline{
    agent{
        label "qwertyy"
    }
        stages{
            stage('buid'){
                steps{
                    sh "mvn clean package"
                }
            }
        }
            stage ('building sonar'){
                steps {
                    withSonarQubeEnv('sonarqube_java_calculator'){
                        sh "mvn sonar:sonar"
                    }
                    
                }
            }
        }
}
                
         
