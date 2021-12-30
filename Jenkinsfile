pipeline {
  agent none
  stages {

    stage('usernamePassword') {
      agent { label 'docker-rzs61' }
      steps {
        script {
          withCredentials([
            usernamePassword(credentialsId: 'docker-q3fzg',
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
