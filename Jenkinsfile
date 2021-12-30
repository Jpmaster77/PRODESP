pipeline {
  agent none
  stages {

    stage('usernamePassword') {
      agent { label 'docker' }
      steps {
        script {
          withCredentials([
            aws(credentialsId: 'jenkins-vfid-ecr',
              accessKeyVariable: 'AWS_ACCESS_KEY_ID',
              secretKeyVariable: 'AWS_SECRET_KEY_ID')
          ]) {
            
            print 'accessKeyVariable'
            print 'secretKeyVariable'
          }
        }
      }
    }
  }
}
