pipeline {
  agent {
    kubernetes {
      defaultContainer 'jnlp'
      yaml """
apiVersion: v1
kind: Pod
metadata:
spec:
  containers:
  - name: busybox
    image: busybox
    command:
    - cat
    tty: true
"""
    }
  }

  stages {
    stage('Run busybox') {
      steps {
        container('busybox') {
          sh 'hostname'
          '
        }
      }
    }
  }
}
