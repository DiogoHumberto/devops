pipeline {
    agent any
    stages{
        stage ('Build do Projeto') {
            steps {
                withMaven (maven : 'maven-latest') {
                    sh '''
                        cd springProject
                        mvn -version
                        mvn clean package -DskipTests
                    '''
                }
            }
        }
    }
}