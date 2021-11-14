pipeline{
    agent any
    stages{
        stage("sonar qyality check"){
           agent {
               docker{
                   image 'openjdk:11'
               }
           }
           steps{
               script{
                   withSonarQubeEnv(credentialsId: 'sonar') {
                       sh 'chmod =x gradlew'
                       sh './gradlew sonarqube'
                   }

                } 
            }
            
        }
    }
}
    
