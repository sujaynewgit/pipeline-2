pipeline {
    agent any
    environment {
    PATH = "/opt/apache-maven-3.9.5/bin:${PATH}"
     }
    stages {
        stage('Clone the Repo') {
            steps {
                git 'https://github.com/devopsgagan/pipeline-1.git'
            }
        }
        stage('Build the Package') {
            steps {
                sh 'mvn clean package'
            }
        }
    }
}
