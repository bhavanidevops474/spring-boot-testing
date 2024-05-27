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
                "mvn clean install" 
            }
            }
        }
        stage('Package') {
            steps {
                script {
                "mvn package -Dmaven.test.skip"
            }
            }
        }
        stage('Publish test results') {
            steps {
                script {
                junit "**/target/surefire-reports/*.xml"
            }
            }
        }
    }
}
