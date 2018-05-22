pipeline {
  agent {
    node {
      label 'pipeline_only'
    }
    
  }
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            sh 'echo "Hello world!"'
          }
        }
        stage('A1') {
          steps {
            echo 'm1-1'
            echo 'm1-2'
          }
        }
        stage('A2') {
          steps {
            echo 'm2-1'
            echo 'm2-2'
          }
        }
      }
    }
    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'Test'
          }
        }
        stage('B1') {
          steps {
            echo 'B1-1'
          }
        }
        stage('B2') {
          steps {
            echo 'B2-2'
          }
        }
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploy'
      }
    }
  }
}