pipeline{
    agent any 
    
    stages{
        stage('SCM Checkout') {
            steps{
                git branch: 'main', url: 'https://github.com/chaksamu/ansible.git'
            }
        }
        stage('Execute Ansible'){
            steps{
                //ansiblePlaybook credentialsId: 'allinone', disableHostKeyChecking: true, installation: 'ansible2', inventory: 'hosts', playbook: 'copy.yml'
                //ansiblePlaybook credentialsId: 'allinone', disableHostKeyChecking: true, installation: 'ansible2', inventory: 'hosts', playbook: 'uploadanduntar.yml'
                //ansiblePlaybook credentialsId: 'allinone', disableHostKeyChecking: true, installation: 'ansible2', inventory: 'hosts', playbook: 'untar.yml'
                ansiblePlaybook credentialsId: 'allinone', disableHostKeyChecking: true, installation: 'ansible2', inventory: 'hosts', playbook: 'nexus.yml'
            }
        }
    }
}
