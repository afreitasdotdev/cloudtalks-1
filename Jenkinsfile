pipeline {
  agent any
  stages {
    stage('Passo1') {
      steps {
        sh 'ls -a'
      }
    }
    stage('Passo2') {
      parallel {
        stage('Passo2') {
          steps {
            sh 'echo "Passo 2"'
          }
        }
        stage('Passo2-a') {
          steps {
            sh 'echo "Passo 2 - a"'
          }
        }
        stage('Passo2-b') {
          steps {
            sh 'echo "Passo 2 - b"'
          }
        }
        stage('Passo2-c') {
          steps {
            sh 'echo "Passo 2 - c"'
          }
        }
      }
    }
    stage('Passo3') {
      steps {
        sh 'echo "Passo 3"'
      }
    }
  }
}