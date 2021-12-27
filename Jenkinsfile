pipeline {
  agent none
  stages {

    stage('usernamePassword') {
      agent { label 'Cacimbinhas-Slave-Suse12' }
      steps {
        script {
          withCredentials([
            usernamePassword(credentialsId: '42d51855-906d-437e-9776-22bbb5c4b6b5',
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
