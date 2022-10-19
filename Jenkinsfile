pipeline {
    agent any
    stages{
        stage ('Build do Projeto') {
            steps {
                sh '''
                    cd springProject
                    apt install maven
                    mvn -version
                    mvn clean package -DskipTests
                '''
            }
        }
    }
}