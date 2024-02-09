pipeline{
    agent any
/*
    tools{

    }

    environment {
        // Define environment variables if needed
        
    }
    */

    stages{
        stage('git chekout'){
            steps{
                sh 'git clone https://github.com/challagondlaanilkumar/web.git '
            }
        }
        stage('soanr'){
            steps{
                withSonarQubeEnv(credentialsId: 'sonar-web-token') {
                    sonar-scanner \
                    -Dssonar.projectKey=web \
                    -Dsonar.sources=. \
                    -Dsonar.host.url=https://sonar.akcdevops.online
               }
            }
        } 
    }
}