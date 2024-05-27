pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                script {
                git branch: 'main', url: 'https://github.com/bhavanidevops474/spring-boot-testing'
            }
            }
        }
        stage('Clean') {
            steps {
                script {
                sh 'mvn clean'
            }
            }
        }
    }
}
