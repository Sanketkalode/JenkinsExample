pipeline{
    agent any
    tools{
        maven 'maven'
        jfrog 'jfrog_cli'
    }
    options { 
    	skipDefaultCheckout() 
    }
    environment{
        CI = true
    }
    stages{
        stage('Clone'){
            steps{
                git 'https://github.com/Sanketkalode/java-web-app.git'
            }
        }
        stage('Build'){
            steps{
                sh 'mvn clean install'
            }
        }
        stage('Deploy Artifactory to Jfrog'){
            steps{
                jf 'rt u target/java-web-app.war java-web-app/'
            }
        }
    }
}