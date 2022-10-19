pipeline {
    agent any
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