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
        sh 'sudo apt update'
        sh '''sudo apt install libc-dev gcc openssl-dev make git libpcap-dev
'''
        sh './configure'
      }
    }
  }
}