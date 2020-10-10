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
	           ansiblePlaybook become: true, credentialsId: '806d90a3-cf7e-4daa-9dc0-97e49b354cfa', installation: 'ansible2', inventory: 'hosts', playbook: 'installtomcat.yml'
                    }
            }
     }
}
