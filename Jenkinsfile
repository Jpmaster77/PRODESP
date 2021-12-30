pipeline {
  agent none
  stages {

    stage('usernamePassword') {
      agent { label 'docker' }
      steps {
        script {
          withCredentials([
            aws(credentialsId: 'jenkins-vfid-ecr',
              accessKey: 'AWS_ACCESS_KEY_ID',
              AWS_SECRET_KEY_ID: 'AWS_SECRET_KEY_ID')
          ]) {
            print 'accessKey=' + username + 'secretKey=' + password

            print 'accessKey.collect { it }=' + accessKey.collect { it }
            print 'secretKey.collect { it }=' + secretKey.collect { it }
          }
        }
      }
    }
  }
}
