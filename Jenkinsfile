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
                sh 'mvn gauge:execute -DspecsDir=specs/conference_app/conference_app_jmeter.spec' 
            }
        }
    }
}
