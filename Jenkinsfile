pipeline{
    agent { 
        label 'agent1'
        }
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
                      echo "THIS IS DEPLOY"
              
                }
            }
        }
    }
}