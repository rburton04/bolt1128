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
        publishHTML([allowMissing: false, alwaysLinkToLastBuild: false, keepAll: false, reportDir: 'reports/html-report', reportFiles: 'index.html', reportName: 'HTML Report', reportTitles: ''])

    }
}
