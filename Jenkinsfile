pipeline {
  agent {
    dockerfile true
  }
  stages {
    stage('set A') {
      steps {
        script {
          A = sh(returnStdout: true, script: 'wc -l')
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