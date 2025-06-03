pipeline{
    agent any
    stages{
        stage('build'){
            steps{
                script{
                      echo "THIS IS BUILD"
              
                }
            }
        }
        stage('test'){
            steps{
                 script{
                      echo "THIS IS TEST"
              
                }
            }
        }
        stage('deploy'){
            steps{
                 script{
                      eho "THIS IS DEPLOY"
              
                }
            }
        }
    }
    post{
        always{
            echo "run always"
        }
        success{
            echo "build is success"
        }
        failure{
            echo "build is failure"
        }
        aborted{
            echo "build is aborted"
        }
    }
}