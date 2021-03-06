pipeline {
      agent any
      stages{
                 stage ( "Git clone") {
                  steps{
                  checkout changelog: false, poll: false, scm: [$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/nduka145/tomcat8.git']]]
		}
	}
                 stage ( "Execute ansible playbook") {
                  steps{
                  ansiblePlaybook become: true, credentialsId: '70825930-7d06-4c06-9b87-1660cdadf7ea', installation: 'Ansible1', inventory: 'hosts', playbook: 'installtomcat.yml'
		}
	}
       }
}
