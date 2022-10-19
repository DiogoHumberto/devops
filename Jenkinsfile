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
        stage ('Testes unit') {
            steps {
                sh '''
                    cd springProject
                    mvn test
                '''
            }
        }
        stage ('Sonar Analysis') {
            enviroment {
                scannerHome = tool 'SONAR_SCANNER'
            }
            steps {
                withSonarQubeEnv('SONAR_LOCAL'){
                    sh '''
                    cd springProject
                    ${scannerHome}/bin/sonar-scanner -e -Dsonar.projectKey=SpringProject -Dsonar.host.url=http://sonarqube:9000 -Dsonar.login=c043ba18afffee57cf75fb300d4a72b9f67aaeec -Dsonar.java.binaries=target -Dsonar.covarage.exclusions=**/.mvn/**,**src/test/**,**model/**,**Application.java
                    '''
                }
            }
        }
    }
}