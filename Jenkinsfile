stage('Build') {
   steps {
       echo 'Building...'
   }
   post {
       always {
           jiraSendBuildInfo branch: 'dev', site: 'greenphysics.atlassian.net'
      }
   }
}
