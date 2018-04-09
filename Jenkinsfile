pipeline {
  agent any
  stages {
    stage('Test') {
      parallel {
        stage('API testing') {
          steps {
            echo 'This is app testing'
          }
        }
        stage('db testing') {
          steps {
            echo 'This is database testing'
          }
        }
        stage('unit testing') {
          steps {
            echo 'this is unit testing of the code'
          }
        }
      }
    }
    stage('Load testing') {
      parallel {
        stage('API load') {
          steps {
            echo 'api load testing'
          }
        }
        stage('db load') {
          steps {
            echo 'db load testing'
          }
        }
        stage('backend load') {
          steps {
            echo 'backend load testing'
          }
        }
      }
    }
    stage('Dev') {
      steps {
        echo 'Deploy to dev encironment'
      }
    }
    stage('Staging') {
      steps {
        sh 'echo "Deploying to staging"'
      }
    }
    stage('Production') {
      steps {
        sh 'echo "deploying to production"'
      }
    }
  }
}