pipeline{
    agent any
    options {
       timeout(time: 10, unit: 'MINUTES') 
       retry(3)
       disableConcurrentBuilds()
    }
    environment{
        project = "expense"
        environment = "dev"
    }   
    stages{
        stage('build'){
            steps{
                script{
                      echo "THIS IS BUILD"
                      echo "project is $project"
                      echo "environment is $environment"
              
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
            input {
                message "Should we continue?"
                ok "Yes, we should."
                submitter "alice,bob"
                parameters {
                    string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
                }
            }
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