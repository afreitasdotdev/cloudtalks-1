pipeline {
  agent any
  stages {
    stage('error') {
      parallel {
        stage('error') {
          steps {
            sh 'sudo docker build -t arfreitas/apache-da-massa .'
          }
        }
        stage('Remove container') {
          steps {
            sh '''sudo docker stop apache-que-funciona
sudo docker rm apache-que-funciona'''
          }
        }
      }
    }
    stage('Docker Run') {
      steps {
        sh 'sudo docker run -d --name apache-que-funciona -p 5000:80 arfreitas/apache-da-massa'
      }
    }
  }
}