pipeline{
    agent any
    environment{
        image = "todo-app"
    }
    stages{
        stage('Github Checkout'){
            steps{
                git branch: 'main', url: 'https://github.com/RohanRusta21/TODO-EXAMPLE-1.git'
            }
        }
        stage('Build Image'){
            steps{
                echo 'Starting to build docker image'
                
                script{
                    customImage = docker.build("${image}:${env.BUILD_ID}")
                }

            }
        }
        stage('Run the Docker Image'){
            steps{
                sh "docker run -itd -p 8000:8000 ${image}:${env.BUILD_ID}"
            }
        }
    }
    
}
