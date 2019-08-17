pipeline {
  agent any
  stages {
    stage('getCode') {
      parallel {
        stage('getCode') {
          steps {
            sh 'ls -lha '
          }
        }
        stage('checaDocker') {
          steps {
            sh 'sudo docker ps -a '
          }
        }
      }
    }
    stage('update') {
      steps {
        sh 'apt-get update'
      }
    }
    stage('Installvim') {
      steps {
        sh 'apt-get install vim'
      }
    }
  }
}