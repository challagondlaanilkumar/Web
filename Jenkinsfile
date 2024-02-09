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
                git branch: 'main', credentialsId: 'github', url: 'https://github.com/challagondlaanilkumar/web.git'
            }
        }
        stage('sonar'){
            steps{
                withSonarQubeEnv('sonar') {
                  sh'''  sonar-scanner \
                    -Dssonar.projectKey=web \
                    -Dsonar.sources=. \
                    -Dsonar.host.url=https://sonar.akcdevops.online '''
               }
            }
        } 
    }
}