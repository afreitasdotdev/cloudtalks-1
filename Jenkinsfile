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

    stage('Passo 2: Buildar container') {
      steps {
        sh "docker build -t arfreitas/cloudtalks:1.0 ."
      }
    }

    stage('Passo 3: Deploy container'){
      steps {
        sh "docker run -d --name apache-que-funciona -p 8686:80 arfreitas/cloudtalks:1.0"
      }
    }
  }
}