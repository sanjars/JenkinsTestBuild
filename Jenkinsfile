pipeline {
    agent any

    // ENV vars
    //environment {
    //    PATH = "/opt/maven3/bin:$PATH"
    //}

    stages {
        stage('Docker Pull the Sonar Scanner CLI Image') {
            steps {
                //
                sh "docker pull sonarsource/sonar-scanner-cli"
            }
        }
        stage('Create Docker Container to Run Sonar Scanner on the source files') {
            steps {
                //
                sh '''
                pwd
                docker run -e SONAR_HOST_URL=http://myhost.com --user="$(id -u):$(id -g)" -i -v "/tmp/sonar-scanning-examples/sonarqube-scanner:/usr/src" sonarsource/sonar-scanner-cli
                ls -lah
                '''
            }
        }
        stage('Scan Finished') {
            steps {
                //
                echo "SonarQube Scanning Finished"
            }
        }
    }
}
