pipeline {
  agent {label "${LABEL_NAME}" }

  stages {
    stage('CODE') {
      steps {
                git url:"" , branch: "main"
      }
    }
    stage('ANSIBLE PLAYBOOK') {
      steps {
        ansibleplaybook(
          playbook: 'ansible/deploy.yml' ,
          inventory: 'ansible/hosts.ini'
        )
    
}
