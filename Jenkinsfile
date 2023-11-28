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
        stage('Test the Package') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Deploy the Package') {
            steps {
                deploy adapters: [tomcat9(credentialsId: 'tomcat-user', path: '', url: 'http://54.167.89.50:8080/')], contextPath: null, war: '**/*.war'
            }
        }
    }
}
