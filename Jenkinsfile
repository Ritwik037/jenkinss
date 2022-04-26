pipeline {
  agent { label 'linux' }
 
  environment {
    DOCKERHUB_CREDENTIALS = credentials('docker_credentials')
  }
  stages {
    stage('Build') {
      steps {
        sh 'docker build -t sample latest .'
      }
    }
    stage('Login') {
      steps {
        sh 'docker login -u' 
      }
    }
    stage('Push') {
      steps {
        sh 'echo $docker_credentials_PSW'
        sh 'echo $docker_credentials_USR'
      }
    }
  }    
//   }
//   post {
//     always {
//       sh 'docker logout'
//     }
//   }
// }