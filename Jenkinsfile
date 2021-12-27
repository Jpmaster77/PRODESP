pipeline {
  agent none
  stdages {

    stage('usernamePassword') {
      agent { label 'Cacimbinhas-Slave-Suse12' }
      steps {
        script {
          withCredentials([
            usernamePassword(credentialsId: 'gitlab',
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
