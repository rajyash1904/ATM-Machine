pipeline {
  agent any
  stages {
    stage('scan') {
      steps {
        sh 'docker run -v ${WORKSPACE}:/src --workdir /src returntocorp/semgrep-agent:v1 semgrep-agent --config p/java --config p/ci --config p/test --config p/r2c-ci'
      }
    }
  }
}
