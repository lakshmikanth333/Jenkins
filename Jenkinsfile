pipeline {
    agent { label 'slave'}
    stages {
        stage('Build') {
            steps {
                sh """
                echo "Hello guru"
                """
            }

        }
          
    }
    post {
        success {
            echo "It got succeeded"
        }
        failure {
            echo "It got failed"
        }
    }

}