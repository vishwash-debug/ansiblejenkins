pipeline {
  agent {label "${LABEL_NAME}" }

  stages {
    stage('CODE') {
      steps {
                git url:"https://github.com/vishwash-debug/ansiblejenkins.git" , branch: "main"
      }
    }
    stage('ANSIBLE PLAYBOOK') {
      steps {
        ansibleplaybook(
          playbook: 'ansible/deploy.yml' ,
          inventory: 'ansible/host.ini' ,
          credentialsId: '${SSH_KEY}'
        )

      }   
    
}
