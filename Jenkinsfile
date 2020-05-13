pipeline {
  agent {
    node {
      label 'java-docker-slave'
    }

  }
  stages {
    stage('Test') {
      steps {
        sh 'node --version'
        sh 'svn --version'
      }
    }

  }
}