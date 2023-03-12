pipeline{
    agent {
        label 'ubuntu'
    }
    
    stages{
        stage('Test agent'){
            steps{
                sh 'ifconfig'
            }
        }
        stage('Print path'){
            steps{
                sh 'pwd'
            }
        }
    }
}