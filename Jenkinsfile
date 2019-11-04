pipeline {
   agent any
    
   options {
       timestamps()
       buildDiscarder(
            logRotator (
               daysToKeepStr: '7',
	       numToKeepStr: '7'
	    )
       )
   }


   stages {
      stage('Build') {
         steps {
	    script {
               currentBuild.description = "build and test UMSL"
	    }
            echo 'Hello World'
	    sh "./mvnw -Pprod clean verify"
         }
      }
   }
}
