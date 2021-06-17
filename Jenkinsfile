pipeline {
  agent {
    dockerfile true
  }
  stages {
    stage('set A') {
      parallel {
        stage('set A') {
          steps {
            script {
              A = sh(returnStdout: true, script: 'wc -l')
            }

          }
        }

        stage('wc -l') {
          steps {
            sh 'wc -l'
          }
        }

      }
    }

    stage('get A') {
      steps {
        echo A
      }
    }

  }
}