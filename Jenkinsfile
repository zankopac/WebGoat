pipeline {
    agent any
    tools {
        maven 'maven_3.8.4'
    }
    stages {
        stage('build') {
            steps {
                echo "Test"
                sh 'mvn --version'
            }
        }
    }
}
