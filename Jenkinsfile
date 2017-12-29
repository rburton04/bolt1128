pipeline {
    agent {
        docker {
            image 'rburton04/bolt-build' 
            args '-v /root/.m2:/root/.m2' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn gauge:execute -DspecsDir=specs/conference_app/UserFeedback.spec' 
            }
        }
    }
}
