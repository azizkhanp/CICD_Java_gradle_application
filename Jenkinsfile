pipeline{

    agent any

    stages{

        stage("sonar quality check"){

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

}
