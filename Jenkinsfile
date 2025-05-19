pipeline {
    agent { label 'slave'}
    stages {
        stage('Build') {
            steps {
                sh """
                echo "Look at the status"
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
        always {
            echo "Always"
        }
    }

}