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

    stage('Test') {
      steps {
        script {
          'chmod +x ./scripts/test.sh'
          'sh ./scripts/test.sh'
        }

      }
    }

  }
  environment {
    registry = 'unloki/cicd_learn'
  }
}