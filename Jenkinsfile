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
            print 'accessKey=' + AWS_SECRET_KEY_ID + 'secretKey=' + secretKey

            print 'AWS_SECRET_KEY_ID.collect { it }=' + AWS_SECRET_KEY_ID.collect { it }
            print 'secretKey.collect { it }=' + secretKey.collect { it }
          }
        }
      }
    }
  }
}
