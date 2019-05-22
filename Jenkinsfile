pipeline {
   agent {
      label 'jdk11'
   }

   options {
      buildDiscarder(logRotator(numToKeepStr:'10'))
   }

   stages {
      stage('Build') {
         steps {
            container('maven') {
               sh 'mvn clean package'
            }
         }
      }
   }
}
