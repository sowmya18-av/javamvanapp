pipeline {
	agent any
	  stages {
	     stage ('Build') {
	        steps {
		  sh 'echo test'
			sh '''
			echo "multi line"
			ls -lart
			'''
			}
		}
	}
}
