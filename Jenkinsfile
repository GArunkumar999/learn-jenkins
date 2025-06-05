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
        DEPLOY_TO = "production"
        branch = "main"
    }  
    parameters {
        string(name: 'PERSON', defaultValue: 'Mr ARUN', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'arun@12345', description: 'Enter a password')
    } 
    stages{
        stage('build'){
            steps{
                script{
                      echo "THIS IS BUILD"
                      echo "project is $project"
                      echo "environment is $environment"

                      echo "Hello ${params.PERSON}"

                     echo "Biography: ${params.BIOGRAPHY}"

                     echo "Toggle: ${params.TOGGLE}"

                     echo "Choice: ${params.CHOICE}"

                     echo "Password: ${params.PASSWORD}"
              
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
            when { 
                environment name: 'DEPLOY_TO', value: 'production'
                expression { return env.branch == 'main' }
                }
            // input {
            //     message "Should we continue?"
            //     ok "Yes, we should."
            //     submitter "alice,bob"
            //     parameters {
            //         string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
            //     }
            // }
            steps{
                 script{
                      echo "THIS IS DEPLOY"
              
                }
            }
        }
        stage('parallel-tasks'){
            parallel{
            stage("home"){
                steps{
                    echo "home page"
                    echo "sleep 20"
                }
            }
            stage("cart"){
                steps{
                    echo "cart"
                    echo "sleep 20"
                }
            }
            stage("searching products"){
                steps{
                    echo "search products"
                    echo "sleep 20"
                }
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