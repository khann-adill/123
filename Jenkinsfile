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
        sh 'echo hi..'
      }
   }
 }
}
