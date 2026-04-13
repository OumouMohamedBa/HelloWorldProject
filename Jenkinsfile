pipeline {
    agent any

    environment {
        ANSIBLE_INVENTORY = 'hosts.ini'
        ANSIBLE_PLAYBOOK  = 'playbook.yml'
        ANSIBLE_HOST_KEY_CHECKING = 'False'
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Vérification Environnement') {
            steps {
                sh 'ansible --version'
            }
        }

        stage('Run Ansible Playbook') {
            steps {
                ansiblePlaybook(
                    playbook: "${ANSIBLE_PLAYBOOK}",
                    inventory: "${ANSIBLE_INVENTORY}",
                    installation: 'ansible',
                    colorized: true
                )
            }
        }
    }
}
