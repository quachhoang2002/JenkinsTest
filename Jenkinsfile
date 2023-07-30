pipeline {
  agent any
  stages {
    stage('checkout_code ') {
      steps {
        git(url: 'https://github.com/quachhoang2002/LapTrinhWeb2.git', branch: 'main')
      }
    }

    stage('check folder ') {
      steps {
        sh 'ls -la '
      }
    }

   stage('Build') { 
      agent {
          docker {
              image 'python:2-alpine' 
          }
      }
      steps {
          sh 'python -m py_compile sources/add2vals.py sources/calc.py' 
          stash(name: 'compiled-results', includes: 'sources/*.py*') 
      }
  }

  }
}