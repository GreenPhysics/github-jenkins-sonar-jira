pipeline {
agent {label 'jenkins_slave'}  
   stages {
         stage('Build') {

             steps {
                   echo 'Building...github-jenkins-sonar-jira'
                  steps {
                        sh 'mvn -B -DskipTests clean package' 
                  }
             }          
             post {
                  always {
                  jiraSendBuildInfo site: 'greenphysics.atlassian.net', branch: 'AD-1'
                }
             }   
         }
    
 }
}
