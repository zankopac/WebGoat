pipeline {
    tools {
        docker 'myDocker'
        maven 'maven_3.8.4'
    }
    agent { docker 'openjdk:15-oracle'  }
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
