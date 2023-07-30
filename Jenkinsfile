pipeline {
  agent any
  stages {
    stage('checkout_code ') {
      steps {
        git(url: 'https://github.com/quachhoang2002/LapTrinhWeb2.git', branch: 'main')
      }
    }

    stage('check folder ') {
      parallel {
        stage('check folder ') {
          steps {
            sh 'ls -la '
          }
        }

        stage('hp') {
          steps {
            sh 'echo "hello my friend " '
          }
        }

      }
    }

    stage('build ') {
      steps {
        sh 'docker ps '
      }
    }

  }
}