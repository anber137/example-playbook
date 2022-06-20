pipeline {
    agent {
        label "ansible_docker"
    }

    stages {
        stage('prepare_node') {
            steps {
                git 'https://github.com/anber137/example-playbook.git'
                sh 'ansible-galaxy role install -r requirements.yml'
                sh 'ansible-playbook site.yml -i inventory/prod.yml'
            }
        }
    }
}
