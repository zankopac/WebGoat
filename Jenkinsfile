pipeline {
    agent { docker 'maven:3.8.4-openjdk-17'  }
    stages {
        stage('startup') {
            steps {
                echo "Test"
                sh 'mvn --version'
            }
        }
        stage('build') {
            steps {
                sh 'mvn --errors --debug clean install'
                sh 'mvn -pl webgoat-server spring-boot:run'
            }
        }
    }
}