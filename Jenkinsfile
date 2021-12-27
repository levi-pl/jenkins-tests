pipeline {
  agent {
    kubernetes {
      yaml """
kind: Pod
metadata:
  name: jenkins-build-agent
  namespace: jenkins
spec:
  containers:
    - name: busybox
      image: busybox
      imagePullPolicy: IfNotPresent
      command:
        - sleep
      parameters:
        - 99d
      tty: true
  restartPolicy: Never
"""
    }
  }
  stages {
    stage('STAGE 1') {
      steps {
        sh 'echo STAGE1'
            }
        }
    stage('STAGE 2') {
      steps {
        sh 'echo STAGE2'
            }
        }
    }
}
