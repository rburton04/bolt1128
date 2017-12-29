pipeline {
    agent {
        docker {
            image 'maven:3-alpine' 
            args '-v /root/.m2:/root/.m2' 
            sh "chmode -R 777 /usr/local/bin"
            sh "curl -SsL https://downloads.getgauge.io/stable | sh"
            sh "gauge install java"

        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn clean install' 
            }
        }
    }
}
