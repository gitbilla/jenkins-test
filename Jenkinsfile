pipeline {
  agent any
  stages {
    stage('ping_test') {
      parallel {
        stage('ping_test') {
          steps {
            sh 'ssh jenkins@ansible \'ansible-playbook -i /extra/ANSIBLE/playbooks/hosts /extra/ANSIBLE/playbooks/pingremote.yml\''
          }
        }

        stage('Build') {
          steps {
            sh 'ssh jenkins@ansible \'ansible-playbook -i /extra/ANSIBLE/playbooks/hosts /extra/ANSIBLE/playbooks/date-time.yml\''
          }
        }

      }
    }

  }
}