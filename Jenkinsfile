#!/usr/bin/env groovy

pipeline  {
stages{
    stage('first stage'){
        sh 'echo "First stage"'
    }
	stage('second sage'){
	    sh 'echo "Second stage"'
	}
		
	stage('third stage'){
         parallel(
			one: {
				echo "This is first branch"
						sh 'pwd'
					},
					two: {
						echo "This is second branch"
						sh 'pwd'
					},
					three: {
						echo "This is third branch"
						echo "Holy Shxt!"
						sh 'pwd'
					},
				)
		}
}
}
