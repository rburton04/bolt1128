
pipeline {
    agent {
        docker {
            image 'rburton04/bolt-build' 
            args '-v /root/.m2:/root/.m2' 
        }
    }
    stages {
        stage('BOLT TESTS') { 
            steps {
                sh 'mvn gauge:execute -DspecsDir=specs/conference_app/conference_app_jmeter.spec' 
            
            
            publishHTML([allowMissing: false, alwaysLinkToLastBuild: false, keepAll: false, reportDir: 'reports/html-report', reportFiles: 'index.html', reportName: 'HTML Report', reportTitles: ''])
           performanceReport parsers: [[$class: 'JMeterParser', glob: '**/*result.xml']], relativeFailedThresholdNegative: 1.2, relativeFailedThresholdPositive: 1.89, relativeUnstableThresholdNegative: 1.8, relativeUnstableThresholdPositive: 1.5
        }
      }
    }
    post {
        always {
            junit '/jmeter/results/results*.xml'
        }
    }

}
