pipeline {
  agent any
  stages {
    stage('Build') {
      agent {
        docker {
          image 'ubuntu'
          args '-u 0'
        }

      }
      steps {
        sh 'apt update'
        sh '''apt install -Y gcc make git libpcap-dev
'''
        sh './configure'
      }
    }
  }
}