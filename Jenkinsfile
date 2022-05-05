pipeline {
	agent any

	  stages {
	     stage ('Build') {
	        steps {
			sh 'mvn -B -DskipTests clean package '

	stages {
		stage('build') {
			steps {
				sh 'echo test'
				sh '''
				echo "multi line"
				ls -lrt 
			  '''
			}
		}
		stage('Test') {
        	steps {
                 sh 'mvn test'
		}
		post {
                 always {
		   junit 'target/surefire-reports/*.xml'
			}
			
		} 	
	}
   stage('Deliver') {
            steps {
                sh './scripts/deliver.sh'
            }
        }
}
}
}
