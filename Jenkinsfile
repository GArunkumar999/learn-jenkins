pipeline{
    agent none
    stages{
        stage('build'){
            agent { label 'agent1' }
            steps{
                script{
                      echo "THIS IS BUILDs"
              
                }
            }
        }
        stage('test'){
            agent { label 'agent1' }
            steps{
                 script{
                      echo "THIS IS TEST"
              
                }
            }
        }
        stage('deploy'){
            agent any
            steps{
                 script{
                      echo "THIS IS DEPLOY"
              
                }
            }
        }
    }
}