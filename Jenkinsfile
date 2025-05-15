pipeline {
    agent any

    stages {
        stage('Run Ansible Playbook') {
            steps {
                sshagent(['mykey']){
                    sh 'ansible-playbook -i inventory.ini playbook.yml'
                }
            }
        }
    }
}
