pipeline {
    agent { label 'slave'}
    environment {
        ENVIRONMENT1 = 'BUILD'
        ENVIRONMENT2 = 'UAT'

    }
    stages {
        stage('Build') {
            steps {
                sh """
                echo "This is $ENVIRONMENT1 area"
                """
            }

        }
        stage('UAT') {
            steps {
                sh """
                echo "This is $ENVIRONMENT2 area"
                """
            }
        }
          
    }
}