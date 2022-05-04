pipeline {
	agent any
	stages {
		stage('build') {
			steps {
				sh 'echo test'
				sh '''
				echo "multi line"
				ls - lrt 
			  '''
			}
		}
	}
}
