pipeline {
    agent any
    stages {
        stage("build the project"){
            steps{
                sh "mvn clean package"
            }
        }
        stage("stop previous running container"){
            steps{
                sh "docker-compose down"  
            }
        }
        stage("run the docker container"){
            steps{
                sh "docker-compose up --build -d"  
            }
        }
    }
}