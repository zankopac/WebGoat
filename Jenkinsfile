pipeline {
    agent {docker { image 'openjdk:15-oracle' }}
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
