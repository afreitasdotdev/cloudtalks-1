pipeline {

  environment {
    NOME = 'teste'
  }

  agent {
    node {
        label 'jenkins-apps'
    }
  }

  stages {
    stage('Primeiro passo a ser executado') {
      steps {
        sh "echo testando..."
      }
    }
  }
}