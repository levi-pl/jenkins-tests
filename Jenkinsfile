pipeline {
  agent {
    kubernetes {
      label podlabel
      yaml """
kind: Pod
metadata:
  name: jenkins-agent
spec:
  containers:
  - name: shell
    image: ubuntu:22.04
    imagePullPolicy: Always
    command:
    - cat
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
