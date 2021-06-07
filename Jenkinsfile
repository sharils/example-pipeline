pipeline {
    agent {
        dockerfile true
    }
    stages {
        stage('Stage Bye') {
            steps {
                sh 'wrk -t2 -c5 -d5s -H "Host: example.com" --timeout 2s http://example.com/index.html'
            }
        }
    }
}
