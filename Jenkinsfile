pipeline {
  agent any
  stages {
    stage('scan') {
      steps {
        sh "docker run --pull always -v ${WORKSPACE}:/src --workdir /src returntocorp/semgrep-agent:v1 semgrep-agent --config s/vicradon:find-all-print-statements"
      }
    }
  }
}
