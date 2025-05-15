pipeline {
    agent any
    stages {
        stages {
        stage('Clone Repo') {
            steps {
                git 'https://github.com/pansel/ansible-demo.git'
            }
        }
        stage('Run Ansible Playbook') {
            steps {
                sshagent(credentials: ['ansible-key']){
                    sh 'ansible-playbook -i inventory.ini playbook.yml'
                }
            }
        }
    }
}
