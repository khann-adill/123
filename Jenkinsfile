pipeline {
   agent any
	 stages {
      stage('Git Checkout') {
         steps {
		       checkout scm
		     }
	 }
   stage('test') {
      steps {
        sh 'echo hi..'
      }
   }
 }
}
