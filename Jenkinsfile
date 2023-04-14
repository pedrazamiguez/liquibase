pipeline {
  agent {
    docker { image 'liquibase/liquibase:4.20' }
  }
  stages {
    stage('Status') {
      steps {
        sh 'liquibase status'
      }
    }
    stage('Update') {
      steps {
        sh 'liquibase update'
      }
    }
  }
  post {
    always {
      cleanWs()
    }
  }
}
