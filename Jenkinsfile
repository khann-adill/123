pipeline {
   agent any
   environment {
	 imagename= 'mak1806/123:latest'
	 dockerImage = ''
	 registryCredential = 'kevalnagda'
	}
   stages {
      stage('Git Checkout') {
         steps {
		       checkout scm
		     }
	 }
   stage('Building image') {
      steps{
        script {
          dockerImage = docker.build imagename
        }
      }
    }
   stage('Deploy Image') {
      steps{
        script {
          docker.withRegistry( '', registryCredential ) {
            dockerImage.push("$BUILD_NUMBER")
             dockerImage.push('latest')
          }
        }
      }
    }
 }
}
