// pipeline {
//   agent any
 
//    environment {
//      docker_credentials = credentials('docker_credentials')
//    }
//   stages {
//     stage('Build') {
//       steps {
//         sh 'docker build -t ritwik72/sample:latest .'
//       }
//     }
//     stage('Login') {
//       steps {
//         sh 'echo $docker_credentials_PSW | docker login -u $docker_credentials_USR --password-stdin'
//       }
//     }
//     stage('Push') {
//       steps {
//         sh 'docker push ritwik72/sample:latest'
        
//       }
//     }
//   }
// }    
// //   }
// //   post {
// //     always {
// //       sh 'docker logout'
// //     }
// //   }
// // }


@Library('docker_library') _

pipeline {
    agent any
  environment {
      docker_credentials = credentials('docker_hub')

  }  
  stages {
      stage('docker-build-push') {
          steps {
              welcome('docker_credentials')
          }

      }
  }
}
