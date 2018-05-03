pipeline {
   agent {
      label 'jdk8'
   }

   options {
      buildDiscarder(logRotator(numToKeepStr:'10'))
   }

   stages {
      stage('Build') {
         container('maven8') {
            steps {
               sh 'mvn clean package'
            }
         }
      }
   }
}
