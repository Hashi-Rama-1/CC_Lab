pipeline {
  agent an
  stages {
    stage('Build'){
      steps {
        build 'PES1UG22CS309-1'
        sh 'g++ task5.cpp -o task5'
      }

    }
    stage('Test'){
      steps {
        sh './task5'
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
