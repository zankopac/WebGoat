pipeline {
    agent any
    tools {
        maven 'maven_3.8.4'
    }
    stages {
        stage('startup') {
            steps {
                echo "Test"
                sh 'mvn --version'
            }
        }
        stage('build') {
            steps {
                sh 'mvn clean install'
                sh 'mvn -pl webgoat-server spring-boot:run'
            }
        }
    }
}
