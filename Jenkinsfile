pipeline {
    agent any
    tools{
        maven 'maven'
    }
    
    stages{
        stage('Clone'){
            steps{
                git 'https://github.com/Sanketkalode/java-web-app.git'
            }
        }
        stage('Builf'){
            steps{
                sh 'mvn clean install'
            }
        }
        
        stage('SonarScan'){
            steps{
                sh 'mvn sonar:sonar \
                  -Dsonar.projectKey=java-web-app \
                  -Dsonar.host.url=http://sonarqube:9000 \
                  -Dsonar.login=26447990a146d30ed101994795bb9fcf97c2e288'
            }
        }
    }
}