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
          'chmod +x ./script.sh'
          'sh ./script/test.sh'
        }

      }
    }

  }
  environment {
    registry = 'unloki/cicd_learn'
  }
}