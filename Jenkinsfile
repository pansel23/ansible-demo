pipeline {
    agent any
    stages {
        stage('Run Ansible Playbook') {
            steps {
                sshagent(credentials: ['ansible-key']){
                    sh 'ansible-playbook -i inventory.ini playbook.yml'
                }
            }
        }
    }
}
