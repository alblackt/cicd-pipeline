pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        script {
          sh 'chmod +x ./scripts/build.sh'
          sh 'scripts/build.sh'
        }

      }
    }

  }
}