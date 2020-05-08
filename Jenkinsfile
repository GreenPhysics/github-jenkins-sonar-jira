pipeline {
stage('Build') {
   agent any
   stages {
         stage('Build') {

   steps {
       echo 'Building...'
   }
   post {
       always {
           jiraSendBuildInfo site: 'greenphysics.atlassian.net', branch: 'AD-1'
      }
   }
  }
 }
}
}
