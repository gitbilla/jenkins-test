pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'Building docker image'
          }
        }

        stage('Test ') {
          steps {
            echo 'Validate the docker image'
          }
        }

      }
    }

    stage('Deploy') {
      parallel {
        stage('Deploy') {
          steps {
            sh '''#!/bin/bash
echo "This is a test script"
echo "Date : `date`"
echo "Hostname : `hostname`"
echo "IP : `hostname -I`"
'''
          }
        }

        stage('test') {
          steps {
            sleep 5
          }
        }

        stage('validate') {
          steps {
            echo 'validation completed'
          }
        }

      }
    }

    stage('prod') {
      steps {
        echo 'Executed on Prod'
      }
    }

  }
}