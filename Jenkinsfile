pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        script {
          sh 'chmod a+x ./scripts/build.sh'
          sh 'scripts/build.sh'
        }

      }
    }

  }
}