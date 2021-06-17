pipeline {
  agent {
    dockerfile true
  }
  stages {
    stage('get example.com') {
      steps {
        sh 'curl http://example.com > example.com'
      }
    }

    stage('keep example.com') {
      steps {
        archiveArtifacts(artifacts: 'example.com', caseSensitive: true, fingerprint: true)
        echo 'ok'
      }
    }

  }
}