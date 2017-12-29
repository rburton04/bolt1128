ipeline {
    agent {
        docker {
            image 'rburton04/bolt-build'
            args '-v /root/.m2:/root/.m2'
       
            }
        }
        stage('Test') { 
            steps {
                sh 'mvn gauge:execute -DspecsDir=specs/conference_app/conference_app_jmeter.spec' 
            }
            post {
                always {
                    junit 'target/surefire-reports/*.xml' 
                }
            }
        }
    }
