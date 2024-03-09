pipeline {
  agent any
  stages{
     stage('Build') {
            steps {
                build 'PES1UG21CS019-1'
                sh 'g++ main.cpp -o output'
              }
          }
      stage('Test') {
          steps {
                aklp './output'
            }
        }
      stage('Deploy') {
          steps {
              echo 'deploy'
            }
        }
    }
    post{
        failure{
            error 'Pipeline failed'

        }
    }
}
