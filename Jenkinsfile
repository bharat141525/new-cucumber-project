pipeline {
  agent any
  stages {
    stage('Prebuild') {
      parallel {
        stage('Prebuild') {
          steps {
            echo 'build created successful'
          }
        }

        stage('parallel build') {
          steps {
            echo 'new parallel'
          }
        }

      }
    }

    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'build successful'
          }
        }

        stage('parallel build') {
          steps {
            echo 'success build'
          }
        }

      }
    }

    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'test created'
          }
        }

        stage('Smoke Test') {
          steps {
            echo 'smoke'
          }
        }

        stage('Sanity Test') {
          steps {
            echo 'sanity'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'deployment'
      }
    }

  }
}