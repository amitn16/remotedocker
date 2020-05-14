pipeline {
  agent {
    dockerfile true
  }
  stages {
    stage('Test') {
      steps {
        sh 'node --version'
        sh 'svn --version'
        node(label: 'remotedocker')
      }
    }

  }
	stage("ssh-agent"){
      script {
        sshagent (credentials: ['9e73bc9-1fe9-455c-8c34-2e8bb0c497a0']) {
          sh 'ssh -o StrictHostKeyChecking=no -l amit 192.168.1.109 uname -a'
			}

		}
    }

}
