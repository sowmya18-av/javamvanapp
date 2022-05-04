pipeline {
	agent any
	stages {
		stage('build') {
		       	steps {
				sh 'mvn -B -DskipTes clean package' 

			      }
			
	                     }
		stage('Test') {
			steps {
				sh 'mvn test'
		              }
						
	        	post {
		           always {
		               junit 'target/surefire-reports/*.xml
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

