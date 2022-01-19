pipeline {
    agent { docker 'maven:3.8.4-jdk-11'  }
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
