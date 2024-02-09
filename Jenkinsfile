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
               sh '''sonar-scanner \
                        -Dsonar.projectKey=web \
                        -Dsonar.sources=. \
                        -Dsonar.host.url=https://sonar.akcdevops.online \
                        -Dsonar.login=sqp_8d2efaa19df0559d769546a30122c2364c57d428'''
            }
        } 
    }
}