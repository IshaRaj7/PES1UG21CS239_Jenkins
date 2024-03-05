pipeline{
  agent any 
  stages {
    stage('Build') {
      steps {
        build 'PES1UG21CS211-1'
        sh 'g++ mai.cpp -o output'
      }
    }
    stage('Test') {
      steps {
        sh './output'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploy'
      }
    }
  }
    post {
      failure {
        error 'Pipeline failed'
      }
    }
}
