pipeline {
    agent {
        docker {
            image 'maven:latest'
            args '--user root -v /var/run/docker.sock:/var/run/docker.sock' // mount Docker socket to access the host's Docker daemon
        }
    }
    
    stages{
        stage (build) {
            steps {
              sh 'mvn -version'
              sh "mvn clean build"
            }
        }
    }
}