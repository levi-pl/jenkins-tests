pipeline {
  agent {
    kubernetes {
      yaml """
kind: Pod
metadata:
  name: jenkins-agent
  namespace: jenkins
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
