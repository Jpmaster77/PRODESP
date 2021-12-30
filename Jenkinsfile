pipeline {
  agent none
  stages {

    stage('usernamePassword') {
      agent any
      steps {
        script {
          withCredentials([
            usernamePassword(credentialsId: 'chandangitpass',
              usernameVariable: 'username',
              passwordVariable: 'password')
          ]) {
            print 'username=' + username + 'password=' + password

            print 'username.collect { it }=' + username.collect { it }
            print 'password.collect { it }=' + password.collect { it }
          }
        }
      }
    }
  }
}
