pipeline {
  agent {
    dockerfile true
  }
  stages {
    stage('get example.com') {
      steps {
        sh 'ls -al > files'
      }
    }

    stage('keep example.com') {
      steps {
        archiveArtifacts(artifacts: 'files', caseSensitive: true, fingerprint: true)
        echo 'ok'
      }
    }

  }
}