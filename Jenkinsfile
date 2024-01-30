pipeline{
    agent any

    environment {
        // Define environment variables if needed
        DOCKER_IMAGE_NAME = 'challagondlaanilkumar/web'
        SONAR_PROJECT_KEY = 'sqp_b6044f0bdf418cae5594e48a88a2e49e8e7daaa5'
        SONAR_HOST_URL = 'http://139.59.36.21:9000'
    }

    stages{
        stage('git chekout'){
            steps{
                sh 'git clone https://github.com/challagondlaanilkumar/web.git '
            }
        }
        stage('soanr'){
            steps{
                cd web
                sonar-scanner \
                -Dsonar.projectKey=web \
                -Dsonar.sources=web \
                -Dsonar.host.url=http://139.59.36.21:9000 \
                -Dsonar.token=sqp_b6044f0bdf418cae5594e48a88a2e49e8e7daaa5
            }
        }
    }
}