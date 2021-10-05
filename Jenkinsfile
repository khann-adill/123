pipeline {
   agent any
	 stages {
      stage('Git Checkout') {
         steps {
		       checkout scm
		     }
	 }
   stage('Build') {
      steps {
        sh 'docker build -t mak1806/123:latest .'
      }
   }
 }
}
