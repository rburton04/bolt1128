
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
                sh 'mvn test-compile'
                sh 'mvn gauge:execute -DspecsDir=specs/conference_app/UserFeedback.spec' 
            
            
             publishHTML([allowMissing: false, alwaysLinkToLastBuild: false, keepAll: false, reportDir: 'reports/html-report', reportFiles: 'index.html', reportName: 'HTML Report', reportTitles: ''])
            //perfReport modePerformancePerTestCase: true, modeThroughput: true, sourceDataFiles: '**/results*.xml'
            hygieiaDeployPublishStep applicationName: 'bolt1', artifactDirectory: '/var/jenkins_home/workspace/bolt-github/reports/html-report', artifactGroup: 'com.bolt.bolt1', artifactName: 'html', artifactVersion: '1.0', buildStatus: 'Success', environmentName: 'Dev'

        }
      }
    }
   
}
