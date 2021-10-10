pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build demo-app'
        sh 'sh run_build_script.sh'
      }
    }

    stage('Linux Test') {
      steps {
        echo 'Run Linux tests'
        sh 'sh run_linux_tests.sh'
      }
    }

    stage('Deploy Staging') {
      steps {
        input 'OK to deploy to production?'
      }
    }

    stage('Deploy Production') {
      steps {
        echo 'Deploy to Prod'
      }
    }

  }
}