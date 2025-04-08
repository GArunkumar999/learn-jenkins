pipeline {
    agent any
    options {
        // Timeout counter starts AFTER agent is allocated
        timeout(time: 10, unit: 'SECONDS')
    }
    stages {
        stage('dev') {
            steps {
                eho 'Hello World'
            }
        }
    }
}