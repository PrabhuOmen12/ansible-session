pipeline {
    agent any

    stages {
        stage('git') {
            steps {
               checkout scm
            }
        }
         stage('ansible-playbook') {
            steps {
                ansiblePlaybook become: true, credentialsId: 'root', disableHostKeyChecking: true, installation: 'ansible', inventory: 'inventory.yml', playbook: 'webserver.yml'
            }
        }
    }
}
