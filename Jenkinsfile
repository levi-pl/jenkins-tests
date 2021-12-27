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
    - name: ubuntu
      image: ubuntu
      imagePullPolicy: IfNotPresent
      command: ["tail", "-f", "/dev/null"]
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
