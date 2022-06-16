pipeline {
    agent any {
        stages {
            stage("git") {
                git "https://github.com/pratsan/devops"
            }
            stage("ansible") {
                sh 'ansible --version'
                ansiblePlaybook(inventory: 'inventories/inventory', playbook: 'playbook.yml')
            }
        }
    }
}