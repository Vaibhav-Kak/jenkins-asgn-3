pipeline {
  agent none
  stages {
    stage('Test Stage') {
      agent {
        label 'Test'
      }
      steps {
        echo 'This is test stage'
        build job: 'Test'
      }
    }

    stage('Prod Stage') {
      agent {
        label 'Prod'
      }
      steps {
        echo 'This is Prod stage'
        build job: 'Prod'
      }
    }

  }
  post {
    success {
      echo "Pipeline completed successfully"
    }
    failure {
      echo "Pipeline failed"
    }
  }
}
