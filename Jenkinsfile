pipeline {
  agent {
    node {
      label 'aaa'
    }

  }
  stages {
    stage('stage1') {
      environment {
        aa = '11'
      }
      parallel {
        stage('stage1') {
          steps {
            sh 'echo \'stage1\''
          }
        }
        stage('ss') {
          steps {
            sh 'echo 123'
          }
        }
        stage('dd') {
          steps {
            echo 'aa'
          }
        }
      }
    }
    stage('stage2') {
      steps {
        echo 'stage2'
      }
    }
  }
}