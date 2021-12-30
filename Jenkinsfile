pipeline {
  agent none
  stages {

    stage('usernamePassword') {
      agent { label 'Windows-Slave01' }
      steps {
        script {
          withCredentials([
            usernamePassword(credentialsId: 'gitlab-token-caas',
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
