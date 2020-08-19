pipeline {
  agent any
  // parameters {
  //   string(name: 'APK_TYPE', description: 'Informar tipo de APK a ser gerado. 1 = HOMOLOG // 2 = BETA // 3 = RELEASE // DEFAULT 0 = DEBUG', defaultValue: '0')
  // }
  stages {
    stage('Passo1') {
      steps {
        sh 'echo $CARAMBA'
        sh 'export MARCELO=CONFIAQUEVAIDARCERTO'
        sh 'echo $MARCELO'
      }
    }
    stage('Passo2') {
      parallel {
        stage('Passo2') {
            when {
              equals(expected: '0', actual: "${params.APK_TYPE}")
            }
          steps {

            sh 'echo "Passo 2 - param 0"'
          }
        }
        stage('Passo2-a') {
            when {
              equals(expected: '1', actual: "${params.APK_TYPE}")
            }
          steps {

            sh 'echo "Passo 2 - a - param 1"'
          }
        }
        stage('Passo2-b') {
            when{
              equals(expected: '2', actual: "${params.APK_TYPE}")
            }
          steps {

            sh 'echo "Passo 2 - b - param 2"'
          }
        }
        stage('Passo2-c') {
            when {
              equals(expected: '3', actual: "${params.APK_TYPE}")
            }
          steps {
            sh 'echo "Passo 2 - c - param 3"'
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