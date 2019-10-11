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
        sh '''apt install -y git
'''
        sh 'apt install -y gcc make  libpcap-dev'
        sh './configure'
      }
    }
  }
}