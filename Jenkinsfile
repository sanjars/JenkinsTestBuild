pipeline {
    agent any

    // ENV vars
    environment {
        PATH = "/opt/maven3/bin:$PATH"
    }

    stages {
        stage('Build') {
            steps {
                //
                echo "Hello World"
            }
        }
        stage('Test') {
            steps {
                //
                echo "testing . . ."
            }
        }
        stage("Maven Build"){
            steps {
                sh "mvn clean package"
            }
        }
        stage('Deploy') {
            steps {
                //
                echo "deploying"
            }
        }
    }
}