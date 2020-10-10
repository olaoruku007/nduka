pipeline {
    agent any
    stages{
            stage('SCM Checkout'){
                    steps{
	           git 'https://github.com/nduka145/tomcat8.git'
                    }
            }
            stage('run ansible playbook'){
                    steps{
	           ansiblePlaybook become: true, becomeUser: 'ansible', credentialsId: '03e6ed82-bdc9-4996-91db-6f066ac3bea3', installation: 'ansible2', inventory: 'hosts', playbook: 'ndukainstall.yml'
                    }
            }
     }
}
