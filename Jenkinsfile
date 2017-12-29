pipeline {
    agent {
        docker {
            image 'maven:latest' 
            args '-v /root/.m2:/root/.m2' 
            

        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'gauge:execute -DspecsDir=specs/conference_app/conference_app_jmeter.spec' 
            }
        }
    }
}
