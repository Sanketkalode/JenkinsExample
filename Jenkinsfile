pipeline {
    agent any
    
    stages{
        
        stage('Email Notification'){
            steps{
                mail to: "kalodes44@gmail.com, kalodesanket@gmail.com", 
                subject: "Build Successful",
                body: "Build Completed Successully ${currentBuild.number}"
            }
        }
    }
}