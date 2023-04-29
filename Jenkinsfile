pipeline {
  agent any
  stages {
    stage('Build') {
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
          sh 'chmod +x ./scripts/test.sh'
          sh './scripts/test.sh'
        }

      }
    }

    stage('Build Docker Image') {
      steps {
        script {
          def customImage = docker.build("${registry}:${env.BUILD_ID}")
        }

      }
    }

    stage('Docker Image Push') {
      steps {
        script {
          docker.withRegistry('https://registry.hub.docker.com', 'docker_hub_creds_id')

          {
            app.push("${env.BUILD_NUMBER}")
            app.push("latest")
          }
        }

      }
    }

  }
  environment {
    registry = 'unloki/cicd_learn'
  }
}