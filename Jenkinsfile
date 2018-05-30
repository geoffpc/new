pipeline {
  agent none
  options {
    buildDiscarder(logRotator(numToKeepStr: '5'))
  }
  stages {
    stage('docker build'){
      agent {	
	docker { image 'node:latest' }
      }
      steps{
        sh "docker -v"
        sh "docker ps"
        sh "whoami"
      }
    }
  }
  post {
    always {
      sh 'echo "This will always run"'
    }
  }
}

