pipeline {
    agent any

    stages {
        stage('Build docker image') {
            steps {
                scripts {
                    bat "docker build -t Clive4216/assignment_9_docker ."
                }
            }
        }
      stage('Build & run docker container') {
          steps {
                scripts {
                    bat "docker run -d --name my-container Clive4216/assignment_9_docker"
                }
          }
      }
    }
}   
