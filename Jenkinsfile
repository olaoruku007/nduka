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
	           ansiblePlaybook become: true, becomeUser: 'ansible', credentialsId: '517a203b-413f-4f86-8d07-9118c86178d0', installation: 'ansible2', inventory: 'hosts', playbook: 'installtomcat.yml'
                    }
            }
     }
}
