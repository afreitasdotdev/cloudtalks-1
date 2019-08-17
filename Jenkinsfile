pipeline {
  agent any
  stages {
    stage('error') {
      steps {
        sh 'sudo docker build -t arfreitas/apache-da-massa .'
      }
    }
    stage('Docker Run') {
      steps {
        sh 'sudo docker run -d arfreitas/apache-da-massa'
      }
    }
  }
}