pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/imahalla/WebApp.git', branch: 'nain')
      }
    }

    stage('log') {
      steps {
        sh 'pwd'
      }
    }

  }
}