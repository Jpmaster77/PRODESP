pipeline {
  agent none
  stages {

stage('list credentials ids') {
  steps {
    script {
      sh 'cat $JENKINS_HOME/credentials.xml | grep "<id>"'
    }
  }
}
