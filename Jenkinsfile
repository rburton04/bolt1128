pipeline {
    agent {
        docker {
            image 'rburton04/bolt-build:latest' 
            args '-v /root/.m2:/root/.m2' 
            

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