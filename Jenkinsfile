pipeline {
    agent any

    stages {
        stage('Test') {
            steps {
                sh "docker run -v $(pwd):/zap/wrk/:rw -t owasp/zap2docker-stable zap-full-scan.py -t http://192.168.100.69/ -g gen.conf -r testreport.html -z '-config scanner.strength=Medium'"
            }
        }
    }
}

