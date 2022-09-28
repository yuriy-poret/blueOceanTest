pipeline {
  agent any
  stages {
    stage('CheckoutGitHub') {
      steps {
        git(url: 'https://github.com/elestopadov/jenkins-example-app.git', branch: 'main')
      }
    }

    stage('Build') {
      steps {
        echo 'This is Build stage'
      }
    }

    stage('Deploy') {
      parallel {
        stage('Deploy to Dev1') {
          steps {
            sleep 30
            echo 'Dev1'
          }
        }

        stage('Deploy to Dev2') {
          steps {
            sleep 50
            echo 'Dev2'
          }
        }

      }
    }

    stage('Test') {
      steps {
        echo 'Testing...'
      }
    }

  }
}