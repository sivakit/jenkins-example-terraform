
pipeline {
  agent any

  stages{
    stage('init') {
      steps {
        container('terraform') {
          sh '''
            echo "test"
          '''
        }
      }
    }

  }
}
