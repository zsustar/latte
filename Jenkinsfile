pipeline {
  agent any
  stages {
    stage('first stage') {
      steps {
        sh 'echo "First stage"'
      }
    }
    stage('second sage') {
      steps {
        sh 'echo "Second stage"'
      }
    }
    stage('third stage') {
      steps {
        parallel(
          "one": {
            echo 'This is first branch'
            sh 'pwd'
            
          },
          "two": {
            echo 'This is second branch'
            sh 'pwd'
            
          },
          "three": {
            echo 'This is third branch'
            echo 'Holy Shxt!'
            sh 'pwd'
            
          }
        )
      }
    }
  }
}