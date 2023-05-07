pipeline{
    agent any
    tools {
        ansible 'ansible'
    }

    stages{
        stage('Copy file to remote server'){
            steps{
                ansiblePlaybook credentialsId: 'ansible', installation: 'ansible', inventory: 'inventory', playbook: 'playbook.yaml'
            }
        }
    }
}