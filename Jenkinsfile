pipeline {
  agent {
    dockerfile true
  }
  stages {
    stage('Stage Bye') {
      parallel {
        stage('Stage Bye') {
          agent any
          steps {
            sh 'wrk -t2 -c5 -d5s -H "Host: example.com" --timeout 2s http://example.com/index.html'
          }
        }

        stage('test') {
          steps {
            sh 'echo \'hello\''
            retry(count: 3) {
              sleep 1
            }

          }
        }

      }
    }

    stage('asdf') {
      steps {
        isUnix()
      }
    }

  }
}