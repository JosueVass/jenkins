pipeline {
  agent any
  stages {
    stage("build") {
      steps {
          echo 'building application'
      }
    }
    stage("test"){
      steps {
          echo 'testing application'
      }
    }
    stage("deploy") {
      steps {
          echo 'deploying application'
      }
    }
  }
  post {
    always {
        junit '**/target/*.xml'
    }
    failure {
        mail to: josue.becerril@vass.com.mx, subject: 'Pipeline failed'
    }
  }
}
