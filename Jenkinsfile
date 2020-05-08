pipeline {
agent {label 'jenkins_slave'}  
   stages {
         stage('Build') {

                  steps {
                        sh 'mvn clean package' 
                  }
             }          
             post {
                  always {
                  jiraSendBuildInfo site: 'greenphysics.atlassian.net', branch: 'AD-1'
                }
             }   
         }
    
 }
