#!/usr/bin/env groovy

node ('master') {
    try {
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
		    stage('Browser Tests'){
      parallel (
        "Firefox": { 
            sh "echo Firefox"
        },
        "Edge": { 
            sh "echo Edge"
        },
        "Safari": { 
            sh "echo Safari"
        },
        "Chrome": { 
            sh "echo Chrome"
        },
      )
    }
    stage('Dev'){
        sh "echo Dev"
    }
    stage('Staging'){
        sh "echo Staging"
    }
    stage('Production'){
        sh "echo Production"
    }
	} catch (error){
		throw error
	}
}
