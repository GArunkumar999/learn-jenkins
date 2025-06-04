pipeline{
    agent any
    options {
       timeout(time: 1, unit: 'SECONDS') 
       retry(3)
    }   
    stages{
        stage('build'){
            steps{
                script{
                      eho "THIS IS BUILD"
              
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
                      echo "THIS IS DEPLOY"
              
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
            deleteDir()
        }
        failure{
            echo "build is failure"
        }
        aborted{
            echo "build is aborted"
        }
    }
}