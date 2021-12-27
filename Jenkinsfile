pipeline {
  agent none
  stages {

    stage('usernamePassword') {
      agent { label 'Cacimbinhas-Slave-Suse12' }
      steps {
        script {
          withCredentials([
            usernamePassword(credentialsId: '435d7e5c-40da-4d27-8848-3739c8341ef1',
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
