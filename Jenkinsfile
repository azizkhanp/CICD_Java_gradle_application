pipeline{
    agent any
    stages{
        stage("sonar quality check"){
            
                docker {
                    image 'openjdk:11'
                }
            }
            steps{
                script{
                    withSonarQubeEnv(credentialsId: 'sonarqube-token') {
                        sh 'chmod +x gradlew'
                        sh './gradlew sonarqube'
            }
            }
           
        }
    }
    
}

