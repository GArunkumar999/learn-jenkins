pipeline {
    agent {
        label 'AGENT-1'
    }
            
   options {
        // Timeout counter starts AFTER agent is allocated
        timeout(time: 10, unit: 'SECONDS')
    }
    stages {
        stage('dev') {
            steps {
                echo 'Hello dev'
                sleep '10'
            }
        }
        stage('QA') {
            steps {
                echo 'Hello qa'
            }
        }
        stage('prod') {
            steps {
                echo 'Hello prod'
            }
        }
    }
}