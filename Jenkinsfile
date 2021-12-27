pipeline {
  agent none
  stages {

    stage('usernamePassword') {
      agent { label 'Cacimbinhas-Slave-Suse12' }
      steps {
        script {
          withCredentials([
            usernamePassword(credentialsId: 'gitops_deploy_key',
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
