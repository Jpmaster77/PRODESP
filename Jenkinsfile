pipeline {
  agent none
  stages {

    stage('usernamePassword') {
      agent { label 'Cacimbinhas-Slave-Suse12' }
      steps {
        script {
          withCredentials([
            usernamePassword(credentialsId: '897f904d-8247-43b4-a21c-3d30b3efdd1e',
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
