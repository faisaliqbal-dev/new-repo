pipeline {
  agent any
  stages {
    stage('build') {
      parallel {
        stage('build') {
          steps {
            echo 'this is building phase'
          }
        }

        stage('shell-script') {
          steps {
            sh '''pwd
ls
date
'''
          }
        }

      }
    }

    stage('test') {
      parallel {
        stage('test') {
          steps {
            echo 'this is testing phase'
          }
        }

        stage('message-test') {
          steps {
            sleep 10
          }
        }

      }
    }

    stage('deploy-on-prod') {
      steps {
        echo 'this is deploying on prod'
      }
    }

    stage('prod') {
      steps {
        echo 'deployed on production'
      }
    }

  }
}