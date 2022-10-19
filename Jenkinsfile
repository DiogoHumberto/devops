pipeline {
    agent any
    stages{
        stage ('Build do Projeto') {
            steps {
                sh '''
                    cd springProject
                    mvn -version
                    mvn clean package -DskipTests
                '''
            }
        }
    }
}