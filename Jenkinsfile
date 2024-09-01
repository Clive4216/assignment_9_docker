pipeline {
    agent any

    stages {
        stage('Build docker image') {
            steps {
                scripts {
                    bat "docker build -t shubham7211/dock ."
                }
            }
        }
      stage('Build & run docker container') {
          steps {
                scripts {
                    bat "docker rm -f my-app-container || exit 0"
                    
                    bat "docker run -d --name my-app-container shubham7211/dock"
                }
          }
      }
    }
}   
