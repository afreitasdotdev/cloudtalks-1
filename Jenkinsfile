pipeline {
  agent any
  stages {
    stage('error') {
      steps {
        sh 'sudo docker build -t arfreitas/apache-da-massa .'
      }
    }
  }
}