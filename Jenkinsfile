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
        parallel(
          "second sage": {
            sh 'echo "Second stage"'
            
          },
          "second last stage": {
            sh 'echo "Second branch stage"'
            
          },
          "Pro Yan": {
            sh 'echo "are you sure that\'s you want to"'
            
          }
        )
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
            echo 'Pro Yan you owe me 2 coffees for pa chong!'
            sh 'pwd'
            
          }
        )
      }
    }
  }
}
