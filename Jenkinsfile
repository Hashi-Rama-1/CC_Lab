pipeline {
  agent any
  stages {
    stage('Build'){
      steps {
        build 'PES1UG22CS335-1'
        sh 'g++ task_5.cpp -o task_5'
      }

    }
    stage('Test'){
      steps {
        sh './task_5.out'
      }
    }
    stage('Deploy'){
      steps{
        echo 'Deployed'
      }
    }
  }
  post{
    failure{
      error 'Pipeline failed'
    }
  }
}
