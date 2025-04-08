pipeline {
    agent {
        label 'AGENT-1'
    }
            
   options {
        // Timeout counter starts AFTER agent is allocated
        timeout(time: 20, unit: 'SECONDS')
    }
    stages {
        stage('dev') {
            steps {
                echo 'Hello dev'
            }
        }
        stage('QA') {
            steps {
                echo 'Hello qa'
            }
        }
        stage('prod') {
            steps {
                echo 'Hello pro'
            }
        }
    }
}