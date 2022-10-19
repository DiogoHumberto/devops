pipeline {
    agent any
    tools {
        maven 'Maven 3.8.6'
        jdk 'Java 1.8'
    }
    stages{
        stage ('Build do Projeto') {
            steps {
                sh '''
                    cd springProject
                    mvn clean package -DskipTests
                '''
            }
        }
    }
}